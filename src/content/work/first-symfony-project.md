---
title: My first Symfony project
publishDate: 2023-06-15 00:00:00
img: /assets/contact-us.png
img_alt: The top of my CV giving a sneak peak into what its design looks like
description: |
  When it comes to making a professional impression, having a strong CV is key. However, creating one that is both informative and visually appealing can be quite a challenge. This process became my next project: crafting a CV that showcases my skills, experience, and personality.
tags:
  - Symfony
  - PHP
  - Doctrine
  - Forms
  - MakerBundle
---

### My First Project with Symfony: Building a Contact Page

In the journey of a software developer, trying out a new technology or framework always holds a sense of adventure. Today, I'd like to talk about my recent exploration into the PHP framework - Symfony.

The task at hand was to create a Contact Page using Symfony. The application would serve as a simple contact form where users can input their name, email, and message. All messages would then be stored in a MySQL database and an admin interface was to be created to allow the reading and deletion of these messages.

##### Diving into Symfony

Coming from a background of working with the Spring framework in Java, I was somewhat familiar with the annotation-based syntax and the concept of external extensions or add-ons. Yet, Symfony was an entirely new playing field for me.

The Symfony framework provides a set of reusable PHP components and a PHP framework to build web applications, APIs, or microservices. Its structure is both comprehensive and complex, offering a powerful platform for developing web applications.

##### The Implementation

My project utilized several significant Symfony components, which include:

Symfony Doctrine: This serves as the Object-Relational Mapper (ORM) and the database abstraction layer. It helped me easily create and manage the database with functions such as doctrine:database:create, doctrine:schema:create, doctrine:migrations:migrate and doctrine:fixtures:load.

Symfony Encore: This is a wrapper around the JavaScript module bundler Webpack. It simplifies the process of working with CSS and JavaScript in Symfony applications.

Symfony Forms: It made the creation of the contact form a breeze with its robust form handling features.

Symfony MakerBundle: This bundle helped me to quickly scaffold code such as controllers, form classes, entities, and tests.

With this setup, the development process was a mix of learning and implementing. From setting up the environment to building the frontend and backend, every step of the process was a deep dive into Symfony.

##### Final Thoughts

This project was a substantial learning experience for me, especially because it was my first time working with Symfony. However, with prior knowledge of frameworks like Spring, I could quickly grasp the fundamentals and complete the project. The process indeed involved a significant amount of learning and dedication.

Moving forward, I am excited to continue exploring Symfony and expanding my knowledge base in the realm of PHP. If you'd like to check out the complete project, you can find it <a href="https://github.com/kiralyzoltan98/contact_page">HERE</a>.
