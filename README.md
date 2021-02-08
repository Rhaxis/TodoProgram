
<br />
<p align="center">

  <h3 align="center">TicTacToe</h3>

  <p align="center">
    Web based ToDo application
    <br />
    <a href="https://github.com/Rhaxis/TodoProgram"><strong>Explore the contents »</strong></a>
    <a href="https://tamk-4a00ez62-3002-group24.herokuapp.com/"><strong>Try the app on Heroku »</strong></a>
    <br />
    <br />
</p>



<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary><h2 style="display: inline-block">Table of Contents</h2></summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#contact">Contact</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project
<img src="Screenshot.png" alt="Screenshot" width="620" height="824">

This program was done as a project work for the React and NodeJS course. It has a database that stores all the inputs and the whole project is deployed to Heroku.
User can add, delete, edit and view tasks in the app. When adding a task user can determine task name, priority and expiration date.

### Built With

* [React](https://reactjs.org/)

* [NodeJS](https://nodejs.org/en/)

* [ExpressJS](https://expressjs.com/)

* [Heroku](https://www.heroku.com/)





<!-- GETTING STARTED -->
## Getting Started

To get a local copy up and running follow these steps.

### Prerequisites

* Java
  ```sh
  https://www.java.com/en/download/
  ```

### Installation

1. Clone the repository to your computer:
   ```sh
   git clone https://github.com/Rhaxis/TodoProgram.git
   ```
2. Move to the directory:
   ```sh
   cd TodoProgram
   ```
3. Install modules using npm
   ```sh
   npm install
   ```
4. Move to frontend directory, install modules:
   ```sh
  cd todo-front
  npm install
   ```
5. Modify API_URL in todo-front/src/APIFunctions.js:
   ```sh
  import axios from "axios"

  const API_URL = "http://localhost:8080/api"
   ```
7. Create a frontend build:
   ```sh
   npm run build
   ```
8. Login to your SQL database and create a table:
   ```sh
  CREATE TABLE todos (
  id int(11) NOT NULL AUTO_INCREMENT,
  name varchar(50) DEFAULT NULL,
  is_done tinyint(1) NOT NULL DEFAULT '0',
  priority int(11) NOT NULL DEFAULT '0',
  date_created timestamp NOT NULL DEFAULT CURRENT_TIMESTAMP,
  deadline date DEFAULT NULL,
  PRIMARY KEY (id)
  );
   ```
9. Insert data into your database:
   ```sh
   INSERT INTO todos(name, is_done, priority, deadline) VALUES("Do the dishes", 0, 5, "2020-12-31");
   ```
10. Edit database/herokuconfig.js file to match your own database:
   ```sh 
  module.exports = {
  host: your_database_url,
  user: your_username,
  password: your_password,
  database: your_database, 
  };
   ```
11. Move to project root and start the app:
   ```sh
   npm start
   ```
12. Open your browser and enter http://localhost:8080/




<!-- USAGE EXAMPLES -->
## Usage

User can assign name, expiration date and priority for the task. After pressing add it gets added to the task list. Its possible to edit and delete the task on the list.



<!-- CONTACT -->
## Contact

Ville Ekholm - ville.ekholm88@gmail.com

Project Link: [https://github.com/Rhaxis/TodoProgram](https://github.com/Rhaxis/TodoProgram)
