---
title: "Event 2"
date: 2026-06-20
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---

# Summary Report: "Tech Tools & Containerization Workshop" - Matching Tools to Roles

### Event Objectives

- Understand the appropriate toolchains for different roles in a modern software development team (Developers, Ops Engineers, Data/ML Engineers).
- Provide a hands-on technical deep dive into Containerization concepts, specifically Docker.
- Explain the basics of container networking and orchestration to prepare participants for deploying scalable applications.

### Speakers

- **Senior Solutions Architect** - AWS (Speaker was an experienced architect with deep knowledge of containerized applications and microservices architectures.)

### Key Highlights

#### The "Right Tool" Philosophy

- The speaker emphasized that tool selection should be based on the problem domain, not just industry hype.
- A matrix was presented showing recommended tools for different roles: Developers focus on `Node.js/Python`, `npm/pip`, `Git`, `VS Code`; Ops Engineers use `Terraform`, `Ansible`, `CloudWatch`, `Prometheus`; Data/ML Engineers rely on `Python`, `Pandas`, `SageMaker`, `Jupyter`.
- The key message was not to force one tool onto everyone, but to understand the unique needs of each role.

#### Understanding Docker in Layers

- Docker was broken down into three conceptual layers:
    1.  **The Image:** A read-only template for creating containers, similar to a class in programming.
    2.  **The Container:** A runnable instance of an image, ephemeral and isolated.
    3.  **The Registry:** A place to store and share images (like Docker Hub or Amazon ECR).
- A simple `Dockerfile` example was demonstrated to show how all configuration is encapsulated, making the application 100% portable.

#### Container Networking: Communication Between Containers

- The workshop covered essential networking concepts:
    - **Port Mapping (`-p 8080:80`)**: Mapping a host port to a container port to allow external access.
    - **Bridge Networks (Default)**: Containers can talk to each other using IP addresses, but IPs can change.
    - **Custom Networks**: The recommended way to connect containers by name, ensuring stable and predictable communication.
- An example showed how a Python script could talk to a containerized MySQL database on the same custom network without exposing the database port to the outside world.

### Key Takeaways

#### Technical Insights

- **Immutability & Reproducibility:** Containers guarantee that an application runs the same way on any environment, which is crucial for ML.
- **Efficiency:** Containers are much lighter than Virtual Machines because they share the host OS kernel.
- **Single Responsibility Principle:** "One service per container" is a best practice for scalability and maintainability.

#### The Challenge of Orchestration

- While Docker is great for running a few containers, managing hundreds manually is a nightmare.
- Kubernetes (K8s) was introduced as an orchestration platform that handles service discovery, load balancing, auto-scaling, and self-healing at scale.

### Applying to Work

- **SageMaker Containers:** Understand that SageMaker training jobs run your code inside a containerized environment; knowledge of containers helps in building custom containers for specific frameworks.
- **Reproducibility:** Instead of just sharing a `.ipynb` file, provide a `Dockerfile` to allow others to set up the exact same environment.
- **Model Serving:** Understand how SageMaker Endpoints work as containerized web servers (e.g., Flask/FastAPI) exposed via port mapping.
- **Microservices:** Design systems as microservices, allowing different parts to be packaged and scaled independently.
- **Local Development:** Use Docker Compose to spin up the full data stack locally to avoid "works-on-my-machine" problems.

### Event Experience

This workshop was the perfect complement to the earlier DevOps session. It gave me the technical foundation to understand how the "Dev" and "Ops" worlds are bridged through containers.

- The concept of `Dockerfile` as a single source of truth for an application's runtime environment was a game-changer.
- It demystified SageMaker: now I see it as simply running a Python script inside a containerized environment exposed via a REST API.
- The networking section taught me how microservices actually communicate, moving beyond simple URL connections.

#### Some event photos

![Participants checking the Dockerfile example during the workshop](/images/4-Events%20Participated/event2.1.jpg)

![Presentation slide showing the container networking architecture](/images/4-Events%20Participated/event2.2.jpg)

> This event significantly improved my understanding of modern application deployment and made me more aware of the underlying infrastructure my ML models rely on.
