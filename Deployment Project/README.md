# Music Playlist API - Backend Project

## Overview

The Music Playlist API is designed to help users manage and interact with their music playlists efficiently. This API provides a range of functionalities such as creating playlists, adding songs, and retrieving playlists or songs. Inspired by an internal database at Warner Music Group (WMG) used to catalog artists and their songs/albums, this project aims to offer a streamlined solution for playlist management.

The primary problem was the lack of a flexible, easy-to-use tool for managing playlists, which could be customized and expanded upon based on user needs.

## Tech Stack:

• Languages: Python
• Frameworks: Flask
• Database: PostgreSQL
• Tools: Postman, locust

## Design and Architecture:

The API is structured to handle various endpoints that manage playlists and songs. This includes creating, deleting, and retrieving playlists and songs, as well as managing relationships between them. Below is a simplified overview of the architecture:

- Database: PostgreSQL stores all data related to playlists and songs.
- API Endpoints: Flask handles requests and interacts with the database.

## Challengs:

One of the major challenges was optimizing database queries for large datasets. I overcame this by implementing indexing strategies and optimizing the query structure to reduce latency.

## Overview of Completed App:

The final API successfully allows users to create and manage music playlists. The core functionalities include:

- Creating, retrieving, updating, and deleting playlists
- Adding, retrieving, and deleting songs from playlists
- Fetching random songs and managing relationships between songs and playlists

## Competencies

### JF 2.4: Can implement effective data management solutions in a project.

**Situation:**  
The Music Playlist API needed to handle large datasets of playlists and songs efficiently, ensuring that data could be retrieved, managed, and manipulated without performance issues.

**Actions:**

- Designed a scalable data management solution using PostgreSQL, which included optimized database schemas and indexing to handle large volumes of data.
- Implemented CRUD operations through Flask, allowing seamless interaction with the database, including the ability to create, retrieve, update, and delete playlists and songs.
- Applied normalization principles to reduce redundancy and improve database efficiency, ensuring quick query response times and optimal performance.

**Results:**  
The API now efficiently handles large datasets with minimal latency, providing a robust and scalable solution for managing playlists and songs.

---

### JF 3.6: Can implement error handling and logging within a project.

**Situation:**  
Reliable error handling and logging were crucial to ensure the stability and maintainability of the Music Playlist API, especially when dealing with a variety of user requests and potential data anomalies.

**Actions:**

- Integrated comprehensive error handling throughout the API, ensuring that all possible exceptions were caught and managed gracefully without crashing the application.
- Implemented logging using Python's built-in logging library to track API usage, errors, and performance metrics. This included logging database query times and failed operations for further analysis.
- Developed custom error messages that provided users with clear feedback, while logging detailed error information for troubleshooting and future improvements.

**Results:**  
The API now handles errors gracefully, providing clear feedback to users while maintaining detailed logs that aid in troubleshooting and improving the system over time.

---

### JF 6.2: Can evaluate and improve the performance of software applications.

**Situation:**  
The performance of the Music Playlist API was critical, especially in terms of handling large data sets and ensuring fast, reliable access to playlist and song information.

**Actions:**

- Conducted performance testing to identify bottlenecks within the API, particularly focusing on database query efficiency and API response times.
- Optimized SQL queries and implemented database indexing to speed up data retrieval processes.

**Results:**  
The API's performance improved significantly, with faster response times and reduced latency, ensuring a smooth user experience even with large datasets.
