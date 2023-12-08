# Step Functions
- to run code in parallel
- to run code in sequence
- in retry
- if then
- overcomes 15 minutes of execution time in lambda
- shows a visual graph as well
- there are 8 states that your machine can be at anytime (pass, task, choice, wait, success, fail, paralle, map)
  - pass: debugging state where you pass input value straight to output
  - task: where work happens
  - wait: A Wait state ("Type": "Wait") delays the state machine from continuing for a specified time.
  - succeed: The Succeed state is a useful target for Choice state branches that don't do anything but stop the execution.
  - fail: A Fail state ("Type": "Fail") stops the execution of the state machine and marks it as a failure, unless it is caught by a Catch block. it will have error message and clause
  - parallel: he Parallel state ("Type": "Parallel") can be used to add separate branches of execution in your state machine.
  - map: Use the Map state to run a set of workflow steps for each item in a dataset. The Map state's iterations run in parallel, which makes it possible to process a dataset quickly. iterate through list of items and perform tasks on them 


### Amazon state language
- json type 

