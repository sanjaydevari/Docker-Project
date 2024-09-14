# `Deployment of Dockerized application in AWS ElasticBeanstalk`
# `Introduction:`
In modern software development, streamlining the process of building and deploying applications is essential for delivering value to users quickly and efficiently. My project focuses on leveraging AWS services, specifically CodePipeline, CodeBuild, and Elastic Beanstalk, to automate the pipeline for building and deploying Dockerized applications.

TechStach:

1.GitHub

2.CodePipeline

3.CodeBuild

4.ElasticBeanstalk

5.Docker : Dockerfile

6.Git, linux, Yaml

# `AWS CodePipeline:`
AWS CodePipeline is a fully managed continuous integration and continuous delivery (CI/CD) service that automates the build, test, and deployment stages of your release process. It allows you to define a series of stages and actions that form a pipeline, enabling the seamless flow of code changes from source to production.

# `GitHub Integration:`
Using GitHub as the source provider in CodePipeline allows us to trigger pipeline execution automatically whenever changes are pushed to the repository. This ensures that our application deployment process remains synchronized with our codebase, promoting consistency and reliability.

# `AWS CodeBuild:`
AWS CodeBuild is a fully managed build service that compiles source code, runs tests, and produces deployable artifacts. By configuring CodeBuild as the build provider in our pipeline, we can define custom build environments and execute build commands specified in our buildspec.yaml file.

# `Buildspec.yaml:`
The buildspec.yaml file serves as the build instructions for CodeBuild, defining the sequence of commands and actions required to build our Dockerized application. It allows us to specify dependencies, build scripts, test commands, and artifact generation, providing full control over the build process.

# `Dockerized Application:`
Docker is a containerization platform that allows us to package our application and its dependencies into a lightweight, portable container. By creating a Dockerfile, we define the environment and configuration for our application container, including base image, dependencies installation, and runtime commands.

# `Elastic Beanstalk Deployment:`
AWS Elastic Beanstalk is a fully managed platform-as-a-service (PaaS) that simplifies the deployment and management of applications. By configuring Elastic Beanstalk as the deployment provider in our pipeline, we can easily deploy our Dockerized application to a scalable and reliable environment.

# `Creation of ElasticBeanstalk Environment`
select the environment-tier as web-server environment

Enter the name of the application

![Screenshot 2024-09-10 161317 1](https://github.com/user-attachments/assets/1732a30e-8eca-456b-bb1d-540de8d14c81)

Enter the name of the environment and check the availability of its domain

Select the platform as managed platform

![Screenshot 2024-09-10 161613 2](https://github.com/user-attachments/assets/ece97270-0f11-44f9-bc0d-bf2425d98183)

Select the application code as sample-application

Select the instance as single-instance(free-tier-eligible)

![Screenshot 2024-09-10 161747 3](https://github.com/user-attachments/assets/94d766d2-72df-46a0-8af3-55458507e60c)

Configure the service access

Create a service role or select the existing one if you have it.

Select the ec2-keypair

Create and select the ec2-instance profile

![Screenshot 2024-09-10 180131 4](https://github.com/user-attachments/assets/c4d39626-0ee5-4363-84d4-4a251dce8c77)

this project doesn't requires any other configurations click on skip all and than on submit

![Screenshot 2024-09-10 180431 5](https://github.com/user-attachments/assets/6dd5e04a-8393-48b1-a7be-d450c5ce1565)

# Creation of pipeline using codepipeline:

![Screenshot 2024-09-10 182303 6](https://github.com/user-attachments/assets/2b76644a-1f51-45c6-90ce-dbff77d2d988)

Enter the name of the pipeline

Select the pipeline-type as V2

![Screenshot 2024-09-10 182453 7](https://github.com/user-attachments/assets/1277559f-08d6-45cc-b147-b23e6afd0920)

Select new-service role

![Screenshot 2024-09-10 182549 8](https://github.com/user-attachments/assets/a27bd903-0c1f-4510-ac8c-4e0765bf924d)

# `SOURCE`
Select the source as GITHUB



