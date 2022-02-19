There are a lot of options for running containers in the cloud, but three of the most popular are AWS EKS, AWS ECS, and Fargate. In this post, we’ll compare and contrast these three services, all in AWS.

![image](https://user-images.githubusercontent.com/99908467/154587690-121b6327-c3a7-4dbc-874b-b4d49400d6c1.png)


**AWS EKS**

AWS EKS is a managed Kubernetes service that makes it easy for you to deploy, manage, and scale Kubernetes clusters. With AWS EKS, you can run Kubernetes on AWS without having to manage Kubernetes clusters or nodes yourself. AWS EKS also gives you the ability to use Kubernetes features such as pods, services, replication controllers, and rolling updates.
AWS EKS is built on top of AWS infrastructure, so you can be confident that your Kubernetes clusters will have the high availability and reliability that you expect from AWS. In addition, AWS EKS is tightly integrated with other AWS services, so you can easily use other AWS services such as Amazon Elastic Compute Cloud (Amazon EC2) instances, Amazon Elastic Block Store (Amazon EBS) volumes, and Amazon Simple Notification Service (Amazon SNS) notifications with your Kubernetes clusters.
To get started with AWS EKS, you first need to create an AWS account and then sign up for AWS EKS. After you sign up for AWS EKS, you can create a new Kubernetes cluster by following the steps in the AWS EKS documentation.

**AWS ECS**

AWS ECS is a container management service from Amazon Web Services. It’s a good choice for organizations that want to use containers, but don’t want to manage the underlying infrastructure. ECS is a good option for both development and production environments.
AWS ECS is a managed container service that enables you to run containers on AWS. It provides a highly scalable, low-cost platform for deploying and managing containers. With ECS, you can launch containers on EC2 instances in a VPC, or you can use AWS Fargate to run containers without managing EC2 instances.
ECS is a powerful service, and there are many things you can do with it. In this blog post, I’ll provide an overview of ECS and show you how to create a simple ECS cluster and deploy a container to it.
ECS Concepts
Before we get started, let’s take a quick look at some of the key concepts involved with ECS.
Container: A container is a self-contained piece of software that includes everything it needs to run, including code, runtime, system tools, and libraries. Containers are lightweight and fast, and they can be used to package and run applications, microservices, and functions.
Cluster: A cluster is a collection of EC2 instances that are used to run containers. You can create a cluster by launching EC2 instances into a VPC, or you can use AWS Fargate to run containers without managing EC2 instances.
Task: A task is a unit of work that is run in a container. A task can be a single container or a group of containers that are run together.
Service: A service is a collection of tasks that are run on a cluster. Services can be used to deploy and manage containers.
ECS Terminology
Now that we’ve covered the basics, let’s take a look at some of the terminology specific to ECS.
Task Definition: A task definition is a JSON file that defines a task. A task definition includes information about the container image, the CPU and memory requirements, and the networking configuration.
Task Group: A task group is a collection of tasks that are run together. Task groups can be used to simplify the management of tasks.
Service Definition: A service definition is a JSON file that defines a service. A service definition includes information about the tasks that make up the service, the environment variables that are used by the tasks, and the networking configuration.
Cluster: A cluster is a collection of EC2 instances that are used to run containers. You can create a cluster by launching EC2 instances into a VPC, or you can use AWS Fargate to run containers without managing EC2 instances.
ECS Cluster
Now that we’ve covered the basics, let’s create a simple ECS cluster.
The first step is to create an ECS cluster. You can do this by using the AWS CLI or the Amazon ECS console.
To create a cluster using the AWS CLI, use the following command:
aws ecs create-cluster — cluster-name my-cluster
To create a cluster using the Amazon ECS console, follow these steps:
1. Open the Amazon ECS console.
2. In the navigation pane, choose Clusters.
3. In the Actions column, choose Create Cluster.
4. Enter a name for your cluster and choose a region.
5. Choose the EC2 instance type that you want to use for your cluster.
6. Choose the VPC that you want to use for your cluster.
7. Choose the number of EC2 instances that you want to use for your cluster.
8. Choose the IAM role that you want to use for your cluster.
9. Choose the networking configuration for your cluster.
10. Review the settings and choose Create Cluster.
The cluster is now created, and you can start using it.
ECS Deployment
Now that we have a cluster, let’s deploy a container to it.
You can deploy a container to a cluster by using the AWS CLI or the Amazon ECS console.
To deploy a container using the AWS CLI, use the following command:
aws ecs deploy — cluster-name my-cluster — service-name my-service — task-definition my-task-definition — count 1
To deploy a container using the Amazon ECS console, follow these steps:
1. Open the Amazon ECS console.
2. In the navigation pane, choose Services.
3. In the Actions column, choose Deploy.
4. Enter a name for your service and choose a cluster.
5. Choose the task definition that you want to use for your service.
6. Choose the number of tasks that you want to run.
7. Review the settings and choose Deploy.
The container is now deployed to your cluster, and you can start using it.

**Fargate**

AWS Fargate is a compute service that enables you to run containers without having to manage servers or clusters. Fargate is an Amazon Web Services (AWS) product that lets you launch containers without having to manage servers or clusters. With Fargate, you simply specify the desired configuration for your containerized application and Fargate takes care of provisioning the underlying compute resources.
AWS Fargate is a compute service that enables you to run containers without having to manage servers or clusters. Fargate is an Amazon Web Services (AWS) product that lets you launch containers without having to manage servers or clusters. With Fargate, you simply specify the desired configuration for your containerized application and Fargate takes care of provisioning the underlying compute resources.
Fargate is an excellent compute service for containerized applications that do not require dedicated resources or persistent storage. Fargate is also a good option for applications that are CPU- or memory-intensive, because Fargate offers you the ability to scale your resources up or down as needed.
If you are new to AWS Fargate, or are considering using it for your next project, here are some things to keep in mind:
1. Fargate is a compute service, not a storage service.
This means that you will need to provide your own storage for your applications if you require persistent storage. Fargate does not currently offer any built-in storage options.
2. Fargate is currently in beta.
This means that there may be some features that are not yet available or that are still in development. If you are considering using Fargate for a production application, be sure to check the current availability of features.
3. Fargate is a good option for applications that require dedicated resources or persistent storage.
Fargate is not a good option for applications that require shared resources or that need to be run on specific servers or clusters. If you are unsure whether Fargate is the right option for your application, be sure to consult the AWS documentation.
4. Fargate is a pay-as-you-go service.
This means that you only pay for the resources that you use. There are no up-front costs or long-term commitments required.
5. Fargate is currently available in the US East (N. Virginia) Region.
This means that if you are located outside of the US East (N. Virginia) Region, you will not be able to use Fargate yet. However, AWS plans to make Fargate available in additional regions in the future.

For more, check out this video: https://www.youtube.com/watch?v=v_j07j6NGZI