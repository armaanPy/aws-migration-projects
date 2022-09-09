# Amazon Elastic Container Service (ECS)

## Container Review
- A container is a unit of software delivery.
- It is a self-contained piece of software that is packaged and executed with all its dependencies.
- Due to its dependencies, containers are very fast to spin up, especially compared to Virtual Machines.
- The container build process allows you to be extremely flexible, you can declare customisations when they are built so you dont need to customise at runtime.
- Thanks to Docker, you are able to package an application on your laptop and have it deployed in production using the exact same image.

## ECS
- Amazon ECS is a highly scalable, high-performance container management service that supports Docker containers and allows you to easily run applications on a managed cluster of EC2 instances.
- ECS eliminates the need for you to install, operate, and scale your own cluster management infrastructure.
- ECS manages the execution of containerised applications in a highly available manner.
- The service manages clusters of instances that support Docker containers, and it monitors resource consumption and availablity requirements.

### Cluster
- An ECS cluster is a group of EC2 instances spread across multiple Availability Zones that are running the ECS container agent.
- The agent is a container itself that allows EC2 instances to talk with the backend logic of ECS, this allows for resource management, lifecycle coordination, and efficient scheduling.

### Task 
- A cluster is where your containers are going to be run, but you'll group containers in what are called tasks, and ask ECS to run them on the cluster.
- Depending on our app needs, we can decide to have a cluster with a mix of instance types and place your tasks accordingly.

### Service
- A service is where all of these functionalities connect together.
- ECS can be configured to schedule tasks based on their definition of a cluster, but with the creation of a service you can have ECS manage the availablity, scalability and lifecycle of your containerised application.
- Creating a service allows you to define the minimum/maximum amount of tasks that you want to run in your cluster.
- Creating a service also allows you to front your application with elastic load balancers, as well as to integrate with a auto-scaling logic.

# Amazon Elastic Container Registry (ECR)

- Amazon ECR is a fully managed Docker image registry that integrates with Amazon ECS, making it easy for you to store, manage and deploy Docker images.
- ECR uses S3 to store images, ensuring high availablity.
- As an AWS service, IAM policies will control access to Amazon ECR, allowing you to manage the access to your storage container images.
- ECR is fully integrated with the Docker CLI, so you can pull or push a container image from or to a repository.  
