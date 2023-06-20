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
