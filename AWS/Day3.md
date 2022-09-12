# Amazon AMI (Amazon Machine Images)

first step is to select an ami when creating an instance <br/>
you can also create your own ami <br/>
there is also an ami marketplace where you can sell, buy and rent your ami
<br/>
<img width="873" alt="amicreated1" src="https://user-images.githubusercontent.com/85761276/188330868-2d6f7036-9f57-49e8-afa5-075139e6d7c0.png"> <br/>

created an instance with the ami<br/>
<img width="782" alt="2" src="https://user-images.githubusercontent.com/85761276/188330919-bca0ef85-52a9-4161-a933-1ca24e42ec3e.png"> <br/>
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AMIs.html

# Amazon EC2 Placement Groups

You can create a placement group using one of the following placement strategies:

1) Cluster placement groups: It is a logical grouping of instances within a single Availability Zone. Cluster placement groups are recommended for applications that benefit from low network latency, high network throughput, or both. They are also recommended when the majority of the network traffic is between the instances in the group. Used for high performance big data jobs. use a single launch request to launch the number of instances that you need in the placement group
2) Partition placement groups:Partition placement groups help reduce the likelihood of correlated hardware failures for your application. When using partition placement groups, Amazon EC2 divides each group into logical segments called partitions.
3) Spread placement groups : A spread placement group is a group of instances that are each placed on distinct hardware. If you start or launch an instance in a spread placement group and there is insufficient unique hardware to fulfill the request, the request fails. Amazon EC2 makes more distinct hardware available over time, so you can try your request again later. restricted to 7 instances per AZ's 



<img width="485" alt="imp questions" src="https://user-images.githubusercontent.com/85761276/189616000-8eb9b497-feac-4eb8-9d7d-a94d1c0ce13c.png">
