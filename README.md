# 42_www_matcha
Creating a dating site using React, Node JS and MySQL

## Intro

Objective of this project is to create a complete dating website that allows users to search, discover profiles according to their preferences and geolocation, show them some love with real-time likes, notifications and chat if both profiles match.

Team of 2: Raphaël ([GitHub](https://github.com/M4sterCiel)) and I.

### Stack

* Node JS (Express)
* React JS
* Materialize CSS and Material UI Front libraries
* Redux JS
* MySQL
* JSON web tokens
* Axios for API requests
* Websockets (socket.io) for real-time
* Google Maps/Geolocator APIs for geolocation

### Features

My Matcha project handles:
* DB creation script
* User creation and authentication using token
* Camera and pictures upload
* Complete user profile page with gender, bio, location, interests details...
* User profile edition (password, details, preferences)
* Profiles discovery based on matching algorithm and user preferences
* Popularity score calculated for each user based on interactions with other profiles
* Profiles search with filters (gender, interests, age and location ranges...) with immediate update
* Real-time notifications for likes, profile views and matches
* Real-time chat if two profiles match
* User ability to block or report another profile
* Email notifications for authentication and password reset (with auth key)
* Change and reset of email/forgot password with ID validation
* Profile, pictures deletion and user DB cleanup
* Responsive design from mobile to desktop/tablet
* User input and upload checks (front/backend)
* Password hashing (Whirlpool)
* HTML/Javascript/SQL injections prevention

Discover more details below.

## User account

### User creation and authentication

User input has been secured on front and back end with immediate feedback for front end input validation. Also password security has been taken seriously with multiple layers of complexity validated on the go, including:
* A lowercase letter
* A uppercase letter
* A number
* A minimum of 8 characters

Password will be hashed (sha512) with a salt for 5 iterations first before being saved in the DB.

![User creation screen with input](https://user-images.githubusercontent.com/45239771/66834447-e6853f80-ef5d-11e9-8bed-7e9f1ce148e9.png)
<p align=center><i>User creation screen with input</i></p>

## Run project

### Environment setup

To run this project, you will need a MySQL database and Node JS server already pre-configured. You can use Bitnami Mamp (MacOS) or Wamp (Windows) for the MySQL database.

The configuration is the following:
* MySQL Database -> Port `3390`
* Node JS server -> Port `8080`
* React app -> Port `3000`

For the web server, we will use an existing Node (Express) JS server, I will explain later how to start it but make sure to have Node and Express installed to run it.

### Create DB

To create the database with already existing users, you can just run the script I have created.

To do so:
* You run it from your shell using command -> `sh back/config/deploy.sh` at root of the project

### Install packages/dependencies

To run the project, you will also need to install some required packages and dependencies, in order to do so:
* Install backend packages/dependencies using command -> `npm i` inside the `back` folder
* Install frontend packages/dependencies using command -> `npm i` inside the `front` folder

### Start servers and website

After having done both previous steps, you can start both MySQL Database from Bitnami software and Node JS server/React app using the following
command -> `npm run dev` from the `back` folder, it will start both.
Then, access the website using the following URL: https://localhost:3000/users/login

Enjoy matches!
[<p align=center>Go up<p>](#42_www_matcha)
