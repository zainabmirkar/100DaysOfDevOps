- resource - it can be any service like ec2, s3 etc
- block - it contains set of information about the infrastructure and what resources are included


# terraform workflow
- write the configuration file
- run the ```terraform init``` command
- review using ```terraform plan``` command
- apply the chnages ```terraform apply```


### Terraform init
- initialize the directory

### Input variables
- reusability of code
- variable types are string, bool, number, any (default)
- others are list, map
- list(string) for a list which consist of string
- type(object) which consists of mixed variable types
- tuple([])

### Variable precedence
- works when we have multiple variables with same name
#### order is as follows
- env
- terraform.tfvars
- *.auto.tfvars
- command line argument


## Resource attributes
- output of one resource as an input for another resource
- ${resource type.resource name.id}

```
 resource "time_static" "time_update" {
}

resource "local_file" "time"{
  content  = "Time stamp of this file is ${time_static.time_update.id}"
  filename = "/root/time.txt"
}
```


## Resource Dependencies
- implicit dependency : when we don't mention what resource is depenedent on which one
- if we want one resource to be created after a specific resource we can mention that using depends_on=[]. This is known as explicit dependency
- when one resource is indirectly dependant on other resource we use explicit dependency


## Output variables
- you can use the terraform output command to display the values of output variables.
- Output variables are also useful when working with Terraform modules.
- You can define outputs in a module and use them as inputs in other modules, enabling data exchange between different parts of your infrastructure configuration.


