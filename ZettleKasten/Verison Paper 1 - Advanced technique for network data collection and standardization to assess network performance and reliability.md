# What to Know Before Reading

To fully grasp the concepts presented in the research paper on evaluating canary deployment techniques using Kubernetes, Istio, and Liquibase, it's essential to have a foundational understanding of several key topics in modern software development and deployment practices. This section will introduce you to these concepts, ensuring you're well-prepared to delve into the detailed notes that follow.

## 1. Continuous Integration and Continuous Deployment (CI/CD)

- **Continuous Integration (CI)**: A development practice where developers frequently integrate code changes into a shared repository. Each integration is verified by automated builds and tests to detect integration errors early.
- **Continuous Deployment (CD)**: An extension of CI where code changes are automatically tested and deployed to production environments, ensuring that software can be reliably released at any time.

**Why It's Important**: CI/CD pipelines automate the software delivery process, allowing teams to deploy code changes more frequently and with higher confidence.

## 2. Microservices Architecture

- **Definition**: An architectural style that structures an application as a collection of loosely coupled, independently deployable services.
- **Benefits**: Enhances scalability, allows for independent development and deployment, and isolates failures.

**Why It's Important**: Microservices facilitate rapid, frequent, and reliable delivery of complex applications, making them ideal for modern cloud-native applications.

## 3. Containerization

- **Definition**: A lightweight, standalone, executable package that includes everything needed to run a piece of software, including the code, runtime, system tools, libraries, and settings.
- **Tools**: Docker is a popular platform for containerization.

**Why It's Important**: Containers ensure that applications run consistently across different computing environments, enhancing portability and scalability.

## 4. Kubernetes

- **Definition**: An open-source platform for automating deployment, scaling, and management of containerized applications.
- **Key Concepts**:
    - **Pods**: The smallest deployable units in Kubernetes, which can contain one or more containers.
    - **Services**: Abstractions that define a logical set of pods and a policy by which to access them.
    - **Deployments**: Kubernetes objects that manage stateless services.

**Why It's Important**: Kubernetes is widely used for orchestrating containerized applications, providing features like automatic scaling, self-healing, and rolling updates.

## 5. Istio

- **Definition**: An open-source service mesh that provides a uniform way to connect, secure, control, and observe microservices.
- **Features**:
    - **Traffic Management**: Controls the flow of traffic and API calls between services.
    - **Security**: Provides service-to-service authentication and encryption.
    - **Observability**: Offers insights into service behavior.

**Why It's Important**: Istio enhances Kubernetes capabilities, especially for managing complex microservices deployments.

## 6. Liquibase

- **Definition**: An open-source database schema change management tool that tracks, versions, and deploys database changes.
- **Features**:
    - **ChangeSets**: Units of change that can be version-controlled.
    - **Contexts**: Tags that control when a changeset should be executed.

**Why It's Important**: Liquibase helps manage database schema changes in a controlled, automated manner, essential for zero-downtime deployments involving database updates.

## 7. Deployment Strategies

Understanding different deployment strategies is crucial for managing application updates without disrupting service.

- **Recreate Deployment**: Stops the old version and then starts the new version, causing downtime.
- **Rolling Deployment**: Gradually replaces instances of the old version with the new one.
- **Blue-Green Deployment**: Runs two identical environments (blue and green) and switches traffic from blue to green when ready.
- **Canary Deployment**: Releases new features to a small subset of users before rolling out to the entire infrastructure.

**Why It's Important**: Each strategy has trade-offs in terms of complexity, risk, and downtime, influencing how organizations deploy applications.

## 8. Load Balancing

- **Definition**: Distributes network or application traffic across multiple servers to ensure no single server bears too much load.
- **Benefits**:
    - Enhances application availability and reliability.
    - Improves performance by optimizing resource use.

**Why It's Important**: Load balancers play a critical role in distributing traffic during deployments, especially in strategies like canary deployments.

## 9. Graceful Shutdown

- **Definition**: A process where an application stops accepting new requests but continues to process ongoing requests before shutting down.
- **Benefits**:
    - Prevents data loss and ensures in-flight transactions complete successfully.

**Why It's Important**: Essential for maintaining data integrity and a seamless user experience during deployments and scaling operations.

## 10. Service Mesh

- **Definition**: A dedicated infrastructure layer that manages service-to-service communication in microservices architectures.
- **Features**:
    - Load balancing, service discovery, encryption, authentication, and authorization.
    - Observability features like tracing and logging.

**Why It's Important**: Service meshes like Istio simplify the complexity of managing microservices by abstracting away network-related concerns.

---

With this foundational knowledge, you're now equipped to understand the detailed notes on the research paper, which explores how these concepts and tools come together to achieve zero downtime deployments in cloud-native enterprise applications.

# Detailed Notes on the Research Paper

## Introduction

### Zero Downtime Deployment

- **Definition**: Deploying new code or bug fixes without any application downtime or service interruption.
- **Importance**:
    - Enhances user experience by ensuring continuous availability.
    - Allows for more frequent deployments and faster iteration.
- **Challenges**:
    - Requires robust methods to integrate and deploy code seamlessly.
    - Complexity increases with microservices and database schema changes.

### Modern Software Development Practices

- **Agile Methods**: Emphasize rapid iteration, close collaboration with business stakeholders, and frequent feedback loops.
- **Microservices Architecture (MSA)**: Breaks down monolithic applications into independent, loosely coupled services that can be developed, deployed, and scaled separately.
- **Containerization and Orchestration**: Use of tools like Docker (containerization) and Kubernetes (orchestration) to manage applications across different environments.

### Paper's Objectives

- **Qualitative Assessment**: Evaluates different code deployment techniques to guide enterprises in choosing the right strategy.
- **Deep Dive into Canary Deployments**: Explores how Kubernetes and Istio can be leveraged to implement canary deployments effectively.
- **Novel Technique**: Presents a method to perform canary deployments for both service and database changes using Istio and Liquibase, achieving zero downtime.

## Continuous Integration and Continuous Deployment (CI/CD)

### Continuous Integration (CI)

- **Process**:
    - Developers frequently commit code to a shared repository.
    - Automated builds and tests are run to detect integration issues early.
- **Benefits**:
    - Improves code quality.
    - Reduces integration problems.

### Continuous Deployment (CD)

- **Process**:
    - Automates the deployment of code changes to different environments (test, staging, production).
    - Ensures that code is always in a deployable state.
- **Benefits**:
    - Accelerates the feedback loop.
    - Enables rapid delivery of features and fixes.

### Traditional vs. Modern Approaches

- **Traditional Deployment**:
    - Manual processes.
    - Long release cycles.
    - Downtime during deployments.
- **Modern Deployment**:
    - Automated pipelines.
    - Frequent, small updates.
    - Aim for zero downtime.

## History and Evolution of Deployment Practices

- **Early Software Development**:
    - Monolithic architectures.
    - Linear, sequential development processes.
    - Integration challenges due to isolated development teams.
- **Introduction of Agile and Extreme Programming**:
    - Emphasis on code quality and responsiveness.
    - Introduction of practices like pair programming, code reviews, and automated testing.
- **Emergence of CI/CD Tools**:
    - **CruiseControl (2001)**: Automated builds and testing.
    - **Jenkins (late 2000s)**: Automated deployment to staging environments.
    - **Configuration Management Tools**: Puppet, Chef for consistent deployments.
- **Rise of Microservices and Containerization**:
    - Microservices allow independent development and deployment of services.
    - Containerization (Docker) packages applications with their dependencies.
    - Orchestration tools (Kubernetes) manage containers at scale.

## Building Blocks for Continuous Deployment

### 1. Modular Design with Microservices

- **Advantages**:
    - Independent development and deployment.
    - Easier scaling and maintenance.
    - Isolation of failures.
- **Comparison with Monolithic Architecture**:
    - Monoliths involve large codebases, making changes and deployments risky and time-consuming.
    - Microservices promote agility and flexibility.

### 2. Containerization

- **Concept**:
    - Containers package applications and their dependencies, ensuring consistency across environments.
- **Benefits**:
    - Portability.
    - Resource efficiency.
    - Simplifies deployment and scaling.
- **Comparison with Virtual Machines (VMs)**:
    - Containers are lightweight and share the host OS kernel.
    - VMs include a full OS, making them heavier.

### 3. Graceful Shutdown

- **Definition**: Allowing an application to finish processing ongoing requests before shutting down.
- **Importance**:
    - Prevents data loss.
    - Maintains service continuity during scaling or updates.
- **Process**:
    - Stop accepting new requests.
    - Complete in-flight requests.
    - Release resources properly.

### 4. Load Balancing

- **Function**: Distributes incoming network traffic across multiple servers.
- **Benefits**:
    - Improves application availability and reliability.
    - Enhances performance by optimizing resource use.
- **Role in Deployments**:
    - Directs traffic during rolling updates or canary deployments.
    - Can help route traffic away from unhealthy instances.

### 5. Health Checks and Traffic Routing

- **Health Checks**:
    - Automated checks to determine if an application instance is healthy.
    - Load balancers use health checks to decide where to route traffic.
- **Traffic Routing**:
    - Dynamic routing decisions based on instance health.
    - Essential for zero downtime deployments.

## Deployment Strategies

### 1. Recreate Deployment (Purge)

- **Process**:
    - Stop the old version entirely.
    - Deploy the new version.
- **Characteristics**:
    - Simple but causes downtime.
- **Use Cases**:
    - Major overhauls where downtime is acceptable.

### 2. Rolling Deployment

- **Process**:
    - Gradually replace old instances with new ones.
    - Old and new versions run simultaneously during the transition.
- **Benefits**:
    - No downtime.
    - Gradual rollout reduces risk.
- **Challenges**:
    - Managing compatibility between versions.

### 3. Blue-Green Deployment

- **Process**:
    - Run two identical environments: blue (current production) and green (new version).
    - Switch traffic from blue to green when ready.
- **Benefits**:
    - Easy rollback by switching back to blue.
- **Challenges**:
    - Requires double the infrastructure during deployment.

### 4. Canary Deployment

- **Process**:
    - Deploy the new version to a small subset of users.
    - Gradually increase the percentage of traffic to the new version.
- **Benefits**:
    - Limits exposure of potential issues.
    - Provides real-world testing.
- **Challenges**:
    - Requires sophisticated traffic routing.
    - Monitoring and metrics are crucial.

### Qualitative Assessment

- **Lead Time for Changes**:
    
    - **Recreate**: Low (but with downtime).
    - **Rolling**: Medium.
    - **Blue-Green**: Medium to High (due to duplicate environments).
    - **Canary**: High (allows for gradual rollout).
- **Cost**:
    
    - **Recreate**: Low.
    - **Rolling**: Medium.
    - **Blue-Green**: High.
    - **Canary**: Medium.
- **User Experience**:
    
    - **Recreate**: Low (downtime).
    - **Rolling**: High.
    - **Blue-Green**: High.
    - **Canary**: High.

## Canary Deployment Workflow and Techniques

### Workflow Steps

1. **Deploy New Version**: Introduce the new version alongside the stable version.
2. **Route a Small Percentage of Traffic**: Begin with a small subset of users.
3. **Monitor Performance**: Collect metrics to assess the new version.
4. **Gradually Increase Traffic**: If metrics are satisfactory, increase traffic to the new version.
5. **Full Rollout or Rollback**:
    - **Rollout**: Transition all traffic to the new version.
    - **Rollback**: Revert to the stable version if issues are detected.

### Challenges with Kubernetes Native Capabilities

- Kubernetes doesn't natively support advanced traffic routing needed for canary deployments.
- Difficulty in controlling traffic percentages between old and new versions using replicas alone.
- Manual scaling of replicas is cumbersome and inefficient.

### Leveraging Istio and Kubernetes Gateway API

- **Istio Service Mesh**:
    - Adds capabilities for fine-grained traffic management.
    - Uses **VirtualService** and **DestinationRule** resources to control traffic routing.
- **Kubernetes Gateway API**:
    - Manages ingress and egress traffic.
    - Provides additional features like logging and observability.

### Two Options for Implementing Canary Deployments

1. **Using Kubernetes Gateway API and Istio**:
    - Separates ingress/egress management from internal service mesh concerns.
    - Offers enhanced observability and logging.
2. **Using Istio Alone**:
    - Simpler architecture with fewer components.
    - Relies on Istio's ingress capabilities.

## Evaluation of Canary Deployment Techniques

### Experiment Setup

- **Application**: A sample microservice (`HelloStats`) deployed on Kubernetes.
- **Deployments**:
    - **Stable Version**: Version 1 with 2 replicas.
    - **Canary Version**: Version 2 with 2 replicas.
- **Tools**:
    - **Istio**: For service mesh capabilities.
    - **Kubernetes Gateway API**: In Option 1.
- **Traffic Management**:
    - Gradually shift traffic from the stable version to the canary version in increments (e.g., 10%, 40%, 90%, 100%).

### Metrics Collected

- **Time Taken for Tests**.
- **Requests per Second**.
- **Time per Request**.
- **Failed Requests**.

### Results

- **Option 1 (Kubernetes Gateway API + Istio)**:
    - Lower requests per second (~6.58).
    - No failed requests.
- **Option 2 (Istio Alone)**:
    - Higher requests per second (~13.15).
    - No failed requests.

### Observations

- **Performance**:
    - Option 2 had higher throughput.
- **Complexity**:
    - Option 1 provides additional features (logging, observability) at the cost of reduced performance.
- **Recommendation**:
    - Choice depends on application needs.
    - If enhanced observability is required, Option 1 is preferable.
    - For higher performance with simpler setup, Option 2 is suitable.

## Canary Deployment with Database Changes

### The Challenge

- Deploying database schema changes without downtime is complex.
- Traditional methods often require taking the database offline.
- Managing multiple schema versions concurrently is difficult.

### Proposed Solution

- **Liquibase**: Used for database schema version control.
- **Expand and Contract Pattern**:
    - **Expand Phase**: Introduce new schema changes while keeping old schema intact.
    - **Contract Phase**: Remove old schema elements once they are no longer needed.

### Implementation Steps

1. **Deploy Stable Version (V1)**:
    - Application runs with current schema.
2. **Deploy Canary Version (V2)**:
    - Introduce new schema changes using Liquibase with **context=expand**.
    - Both old and new schema coexist.
3. **Gradually Shift Traffic**:
    - Route a small percentage of traffic to V2.
    - Monitor for issues.
4. **Fully Transition to V2**:
    - Once stable, route all traffic to V2.
5. **Contract Phase**:
    - Deploy V2 with **context=contract**.
    - Remove old schema elements.
6. **Decommission V1**:
    - Remove the old version of the application.

### Benefits

- **Zero Downtime**: Users experience no interruption during the deployment.
- **Data Integrity**: In-flight transactions are preserved.
- **Simplified Rollback**: If issues arise, traffic can be redirected back to V1.

### Reference Architecture

- **Components**:
    - **Kubernetes**: Manages application deployment.
    - **Istio**: Handles traffic routing between service versions.
    - **Liquibase**: Manages database schema changes.
    - **Load Balancer**: Distributes traffic based on routing rules.