### You have a specific application that requires its components to be placed on nodes after performing some additional checks?
- So you decide to have your own scheduling algorithm to place pods on nodes so that you can add your own custom conditions and checks in it.
- You can write your own Kubernetes scheduler program, package it and deploy it as the default scheduler or as an additional scheduler.
- When creating a pod or a deployment, you can instruct Kubernetes to have the pod scheduled by a specific scheduler.
- create a scheduler.yaml file
- If multiple copies of the same scheduler are running on different nodes, only one can be active at a time, and that's where the leader elect option helps in choosing a leader
who will lead the scheduling activities. (HA setup)

