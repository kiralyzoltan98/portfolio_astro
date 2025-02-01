---
title: Full-Stack? All-Stack!
publishDate: 2025-01-12 00:00:00
img: /assets/rtree.png
img_alt: A diagram of the projects infrastructure.
description: |
    Infrastructure-Driven Development
tags:
    - Java
    - Spring Boot
    - Podman
    - DevOps
    - Makefile
---

### The Challenge
Recently, I set out to challenge myself with a full-stack DevOps-oriented project that went beyond just coding a simple application. While the core functionality was straightforward—a Spring Boot app with two endpoints—the real challenge lay in the architecture, automation, and containerization constraints I had to work within.

This wasn’t just about writing Java code; it was an opportunity to learn, experiment, and refine my skills in infrastructure management, CI/CD automation, and containerized deployments.

### The Core Application
At its heart, the project is a recursive file discovery tool, built with Spring Boot. The application provides two main endpoints:

GET `/getunique` : Accepts a file path and returns a list of all unique filenames found within that directory (recursively). The response also includes a timestamp and the user who made the request. Additionally, I added a file extension filter to allow users to refine their searches.

GET `/history` : Retrieves previously stored results from a MariaDB database, allowing users to query past searches by username, timestamp, or file results.

##### I also went the extra mile and implemented some features that makes trying the application out easier:
PUT `/generate` : This endpoint creates a test file structure to make it easier for users to validate the tool's functionality. The generated files cover various extensions (e.g., .txt, .json, .yaml, .c), allowing flexible testing.

### Containerized Architecture with Podman
One of the key constraints in this project was that everything had to run in containers using Podman. I structured the system with at least two instances of the application running simultaneously, each on ports 8081 and 8082.

The application instances and the database run in separate containers, all orchestrated by a custom Makefile that handles:
 - Building the images
 - Starting the database
 - Running the application instances

Additionally, the setup ensures that users don’t need Java installed on their system. Instead, the application is built inside a container, isolating dependencies and providing a self-contained execution environment.

### Automation & CI/CD with GitHub Actions
To ensure everything works smoothly, I implemented GitHub Actions to:
 - Run unit tests on every push or PR
 - Build the project and validate its correctness
 - Publish the images to Docker Hub

With this setup, anyone can clone the repo, run make run, and the entire system assembles itself—a perfect example of infrastructure-as-code.

### Engineering Decisions & Key Takeaways
 1. Database Choice: I went with MariaDB, using an official image from Docker Hub. The database schema is minimal, consisting of a single history table to store search results.
 2. Code Quality: Implemented unit tests to ensure the core logic works correctly, especially around filtering unique files.
 3. Error Handling: Used Spring’s @ControllerAdvice for a global exception handler, ensuring consistent error responses.
 4. Documentation: Generated Javadoc for the codebase and made Swagger UI available at /doc on both app instances.
 5. Makefile Over Shell Scripts: The project relies solely on Makefiles for automation—no Bash scripts—adding an extra layer of challenge.

### Final Thoughts
This project was a great deep dive into automation, DevOps, and containerized infrastructure. While the Spring Boot application itself was simple, the focus was on how to structure, deploy, and automate an entire system efficiently.

By implementing CI/CD pipelines, containerized deployments, and infrastructure automation, I took this beyond just a Java project and turned it into a full-fledged DevOps challenge.

I have heard in a podcast that a developer who has a clear idea of how and where the code runs writes better code and I can say that this project was a great way to learn about that.

In my opinion there is also a modern trend toward "shift-left" practices, where developers take on more operational responsibilities and need to understand the entire technology stack from top to bottom.

#### Want to try it out? Clone the repo and run:
``` sh
git clone https://github.com/kiralyzoltan98/rtree.git
cd rtree
make run
```
And you’re up and running!

##### Check out the project <a href="https://github.com/kiralyzoltan98/rtree">HERE</a>
