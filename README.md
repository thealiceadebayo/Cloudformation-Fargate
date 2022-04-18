# Cloudformation-Fargate
Automate The Deployment of Docker Images with AWS CloudFormation

<br> <b> Project Goal </b>

Create a production-grade, continuously deployable system.

<b> Cloudformation Stack Design </b>

![image](https://user-images.githubusercontent.com/88491497/163741513-a820d70a-f863-4802-aa12-d3e2d90c491a.png)

two CloudFormation stacks:

A network stack that creates a VPC (virtual private cloud) with two public subnets (each in a different availability zone for high availability), an internet gateway, and a load balancer that balances traffic between those networks.
A service stack that places a Docker container with the application we want to run into each of the public networks. For this, we take advantage of ECS (Elastic Container Service) and Fargate, which together abstract away some of the gritty details and make it easier to run a Docker container.
