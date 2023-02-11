- when you launch an instance, it comes with a network interface attached to it and that will have a private IP address.
- And then in some cases, it can also have a public IP address if it's in a public subnet.

- we could not attach an adapter from a subnet in another availability zone, that just won't work.
- you can have multiple adapters connected to an instance.
- They can be in different subnets, but the subnets have to be in the same availability zone.

# Network Interfaces
- elastic network interfaces
- elastic network adapters
- elastic fabric adapters

# Difference 
- the ENI is the basic adapter for when you don't have any specific high performance requirements. And you can use it with any EC2 instant's type.
- The elastic network adapter is for enhanced networking performance. It has much higher bandwidth and lower inter-instance latency. You have to choose supported instance types. You can't use any instance type with an ENA.
- Lastly, we have the elastic fabric adapter. This is for more specialized use cases. You use this for high performance computing, HPC and MPI and ML use cases.
It's for tightly coupled applications, so those applications, which will typically be in low latency environments where they're very close to each other and they have a lot of
inter-connectivity between them. Lots of messaging happening between components of the application. You can use those with all instance types, but again, you would only use them when you have a specific use case.


# More info
- eip can be attached to network interfaces as well.
- eips can be remapped across az but network interfaces can't
