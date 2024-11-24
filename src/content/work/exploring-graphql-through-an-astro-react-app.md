---
title: Exploring GraphQL through an Astro-React App
publishDate: 2024-04-01 00:00:00
img: /assets/tech-stack.png
img_alt: The logo of Astro, React, GraphQL, ExpressJS and Mongodb the technologies I used for this project.
description: |
  GraphQL, an open-source data query and manipulation language for APIs, has always intrigued me with its numerous features. The possibilities seemed endless, and I was eager to dive into it. To get a hands-on experience, I decided to build a simple app using Astro with some React components, complemented with an Express.js backend and a cloud MongoDB database.
tags:
  - Astro
  - React
  - GraphQL
  - Express.js
  - MongoDB
---

### The Frontend: Astro and React

The frontend of my app was an exciting blend of Astro and React components. The primary task here was to put together a dynamic query - not quite a traditional query, but more of a flexible selection of checkboxes. This setup allowed the frontend to communicate user's requests effectively to the backend, ensuring that the data returned was custom-tailored to the user's preferences.

##### The Backend: Express.js and MongoDB

Express.js is a robust, fast, and unopinionated web application framework for Node.js. With its syntax based on JavaScript, I was able to grasp its working quickly. I chose MongoDB as my database for this project - an excellent choice for cloud databases due to its scalability and flexibility.

For interacting with MongoDB, I used Mongoose - a MongoDB object modeling tool. Mongoose provides a straightforward, schema-based solution to model our application data. It also includes built-in type casting, validation, query building, and business logic hooks.

##### The Bridge: GraphQL API

The most exciting part of the project was implementing a GraphQL API. This API was crucial as it served as the bridge between the dynamic 'query' formed in the frontend and the database. Through the API, the user-made query from the frontend could fetch exactly the data needed from the MongoDB backend.

This project was a fantastic learning journey - from enhancing my understanding of Astro and React components to getting my hands dirty with Express.js, MongoDB, and Mongoose. However, the cherry on the cake was diving into the world of GraphQL and experiencing first-hand its power and flexibility in managing API requests and responses.

##### Check out this project on GitHub <a href="https://github.com/kiralyzoltan98/expressjs_graphql_mongodb_backend">HERE</a>
