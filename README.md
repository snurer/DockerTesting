# Dockerizing a Simple Node.js Application

This repository contains a simple "Hello World" Node.js application that has been dockerized for easy deployment.

## Contents

- [Dockerfile](https://github.com/snurer/DockerTesting/blob/main/Dockerfile): The Dockerfile defines the instructions for building the Docker image. It starts with the official Node.js image, sets the working directory, copies the package.json and package-lock.json files, installs application dependencies, copies the rest of the application files, exposes the necessary port, and specifies the command to start the application.

- [app.js](https://github.com/snurer/DockerTesting/blob/main/app.js): This is the main application file that contains the code for a basic HTTP server. It listens on a specific port and responds with a "Hello, World!" message when a request is made to the server.

- [package.json](https://github.com/snurer/DockerTesting/blob/main/package.json): The package.json file manages the dependencies and configuration of the Node.js application. It includes metadata about the project, specifies the main application file, defines scripts to run various tasks, and lists the necessary dependencies. In this case, it includes the express package as a dependency.

## Usage

To run the application locally without Docker, ensure that you have Node.js and npm installed on your machine. Then, follow these steps:

1. Install dependencies by running the following command:

``` npm instal ```

2. Start the server by running the following command:

``` npm start ```
This will start the server and it will be accessible at `http://<host>:3000/`. You should see a "Hello, World!" message when you visit that URL in your web browser.

To run the application using Docker, follow these steps:

1. Make sure you have Docker installed on your machine.

2. Build the Docker image by running the following command:

``` docker build -t my-node-app . ```

3. Run a container based on the built image using the following command:

``` docker run -p 3000:3000 my-node-app ```

The containerized application will be accessible at `http://<host>:3000/` in your web browser.

In my case, it's http://54.86.130.225:3000/

Author: [snurer](https://github.com/snurer)
