## Route 53

- domain name registration
- dns management
- traffic management
- uses edge locations

## Intorduction

- DNS translates domain name into ip addresses

### Hosted Zones
- A hosted zone is a container for records, and records contain information about how you want to route traffic for a specific domain, such as example.com, and its subdomains (acme.example.com, zenith.example.com).
- A hosted zone and the corresponding domain have the same name. There are two types of hosted zones:
- Public hosted zones contain records that specify how you want to route traffic on the internet.
- Private hosted zones contain records that specify how you want to route traffic in an Amazon VPC.

### Private hosted zones
- To use private hosted zones, you must set the following Amazon VPC settings to true: enableDnsHostnames and enableDnsSupport

### Types of record
- A Record IPv4 address record : used to map a hostname to an ip address
- AAAA Record ipv6 : used to map a hostname to an ip address
- mail exchnage record : used to identify email servers for a given domain
- text record: used to provide info in a txt format to systems outside of your domain
- cname: map a hostname to another hostname
- alias: maps a custom hostname in your domain to an aws resource

### Helath checks
- Health checks that monitor an endpoint
- Health checks that monitor other health checks (calculated health checks)
- Health checks that monitor CloudWatch alarms
- every 30 seconds if you soecif then 10 seconds

### Routing policies
- the routing policy for a record defines ohow to answer dns query
- simple : assigns ip to a record at random. does not support hea;th checks
- weighted: Let's say you have two servers, Server A with a weight of 1 and Server B with a weight of 2. For every three DNS queries, Route 53 will send one query to Server A and two queries to Server B.
- geolocation: Use when you want to route traffic based on the location of your users
- geoproximity: these records are tagged with an aws region or using latitude or longitude coordinates. it is based on diatnce and defined bias.
bias is from 99 to -99. route more traffic thorgh positive value and less through negative value
- failover routing policy: redirects traffic based on health checks
- latency: uses the lowest latency to redirect to cutomer
- multi value answer: returns multiple ip addresses to the query. upto 8 ip are returns based on health checks. if there are 8 or less helathy hosts then all are returned

### Traffic flow
- this is useful when you have multiple servers that perform the same operation
- You can create records one at a time, but it's hard to keep track of the relationships among the records when you're reviewing the settings in the Route 53 console.
- can include multiple policies and health checks in the same configuration
- it is called traffic policy and is automatically versioned
- old versions will be available until you delete them
- geoproximity is only available when using traffic flow
- Traffic flow greatly simplifies the process of creating and maintaining records in large and complex configurations.
(traffic flow doc)[https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/traffic-flow.html]


### Resolver
-

### Application recovery controller
- Amazon Route 53 Application Recovery Controller gives you insights into whether your applications and resources are ready for recovery.
- The Application Recovery Controller also helps you manage and coordinate recovery for your applications across AWS Availability Zones (AZs) or Regions.
- These capabilities make application recoveries simpler and more reliable by reducing the manual steps required by traditional tools and processes.





































