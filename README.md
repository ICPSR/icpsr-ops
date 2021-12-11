# icpsr-ops
ICPSR's Cloud Native development and deployment with GitOps and Kubernetes.


# History

ICPSR had a variety of traditional monolithic web applications hosted on dedicated servers. This was inefficient, did not scale well as usage increased, and was difficult to maintain. To address the issues, the functionality needed to be separated out into separate microservices and deployed as containers on Kubernetes clusters.  

# Methods

ICPSR followed several steps to transition from monolithic applications on traditional server hardware and  Virtual Machines to Kubernetes in the cloud.

* Refactored monolithic application code into task-focused microservices/libraries.
* Deployed two separate Kubernetes clusters: one for the development and one for hosting completed applications.
* Stored all application code and cluster configuration in the UM Gitlab repository.
* Automated the process of loading computer code and cluster configuration continuously. (“GitOps”)

# Results

* Developers can spin up new web applications without server admin intervention, including building one-off instances to test functionality.
* The microservices/libraries can be reused, speeding up the creation of new web applications.
* Applications are more resilient, as the code and settings can be reloaded from Git in moments.
* The state of the cluster is maintained through an automated reconciling of the stored configuration. 
