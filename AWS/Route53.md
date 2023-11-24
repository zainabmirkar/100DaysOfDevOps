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











