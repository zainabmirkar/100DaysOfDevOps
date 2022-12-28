# What do you do when you do not have a scheduler in your cluster?

- Let's start with a simple pod definition file. Every pod has a field called Node Name that, by default, is not set.
- You don't typically specify this field when you create the pod manifest file.
- Kubernetes adds it automatically.
- The scheduler goes through all the pods and looks for those that do not have this property set.
- Those are the candidates for scheduling. It then identifies the right node for the pod by running the scheduling algorithm.
- Once identified, it schedules the pod on the node by setting the node name property to the name of the node by creating a binding object.

### Manually assign the pod to a node
- You can manually assign pods to nodes yourself. Well, without a scheduler, the easiest way to schedule a pod is to simply set the node name field to the name of the node
in your pod specification file while creating the pod. The pod then gets assigned to the specified node. You can only specify the node name at creation time.

- Also, another way to assign a node to an existing pod is to create a binding object and send a POST request to the pod's binding API. In the binding object, you specify a target node
with the name of the node, then send a POST request to the pod's binding API with the data set to the binding object in a JSON format.
- So you must convert the YAML file into its equivalent JSON form.


#### Also read
https://www.waytoeasylearn.com/learn/kubernetes-manual-scheduling/
