## VPC Peering

- 2 vpc's to communicate with each other
- can be diffrent/ same regions
- one to one connection only
- there should'nt be any ip addresses overlapping for any vpcs
- vpc 1 should send vcp peering request to vpc 2
- vpc 1 is 10.0.0.0/16 and vpc 2 cidr block is 172.31.0.0/16
- route table should be updated acc to cidr block

![image](https://github.com/zainabmirkar/100DaysOfDevOps/assets/85761276/c008a03f-0c12-4725-bf9a-424db342901b)

## Transit gateway

- when there are many vpcs and remote office locations then creating vpc peering connections between each one of them can be very difficult
- transit gateway helps us to manage that by creating a central location and all the vpc and remote locations connect to that central location
- there can be direct connect, private gateways and customer gateways

![image](https://github.com/zainabmirkar/100DaysOfDevOps/assets/85761276/f0121dcd-a464-4370-b83e-d66320188c28)
