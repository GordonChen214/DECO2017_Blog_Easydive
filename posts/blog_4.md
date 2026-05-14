---
title: Website Data Structure and Technical Feasibility Analysis
date: 2026-04-29
author: Guanwei Chen
summary: This blog is based on functional and user flow design, analyzing the feasibility of the Easy Dive platform from the perspectives of data structure, system relationships, and technical implementation, and making reasonable trade-offs within its own technical scope.
tags:
  - data-structure
  - database-design
  - technical-feasibility
---
Based on the preliminary functional analysis and user flow design, the focus of this stage is to further transform the concept of the Easy Dive platform into realizable data structures and technical solutions. According to the course content, system design is not only a combination of functions, but also an overall consideration of 'how data is organized, related, and used'.

First, from the perspective of data modeling, this project needs to clarify the core entities in the system and their relationships. Combining with the preliminary design, multiple key data objects can be identified, including Users, Dive Sites, Dive Plans, and Participation Records. According to the course's introduction to relational databases, data should be stored in a structured form and organized through tables, columns, and primary keys, thereby supporting efficient data querying and management.

Looking further, these data do not exist in isolation, but form an interconnected system. For example, a diving plan links users with dive sites, while participation records describe the relationships between multiple users and the plan. This design reflects the 'systems thinking' emphasized in the course, meaning that the value of the system lies not only in individual data items, but more in the relationships between the data.

Based on this structure, this project chooses to use SQLite as the database solution. Compared with a simple JSON file, a database can provide a more stable way of storing data and supports complex query operations, such as filtering dive sites or dive plans that meet specific conditions. In addition, the database can also enforce constraints on data types, thereby avoiding data inconsistency issues.

At the system implementation level, the project builds the backend logic based on the MojoJS framework. MojoJS is responsible for handling HTTP requests and responses, and returns the corresponding page content according to different routes. This server-driven dynamic generation method allows the system to provide different data content in real time based on user behavior, thereby achieving a truly "data-driven" application.

In terms of user interaction, this project is designed around CRUD (Create, Read, Update, Delete) operations. For example, users can create diving records (Create), browse dive site information (Read), update personal profiles (Update), and delete unnecessary records (Delete). These operations are implemented through HTML forms and HTTP requests, combined with HTMX technology to support partial page updates, allowing interactions to be completed without refreshing the entire page, thereby enhancing the continuity of the user experience.

However, during the process of implementing the functionality, it is also necessary to control the technical complexity. For example, if the companion matching feature were to use an automatic recommendation algorithm, it would involve complex data processing and logical judgment, which is beyond the technical scope I currently master. Therefore, this project chooses to implement the basic matching function by allowing users to browse companion information and proactively match themselves. Similarly, the real-time chat feature is also regarded as a potential extension direction, rather than a core implementation of the current prototype.
