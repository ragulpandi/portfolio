# Portfolio Website Deployment Guide

This guide will walk you through the process of cloning the [Portfolio Website](https://github.com/ragulpandi/portfolio) repository, setting up Node.js, bundling the project, and deploying it to Firebase.

## Prerequisites

- Git
- Node.js and npm
- Firebase CLI

## Cloning the Repository

1. Open your terminal.
2. Clone the repository using Git:
   ```bash
   git clone https://github.com/ragulpandi/portfolio.git
   ```
3. Navigate to the cloned directory:
   ```bash
   cd portfolio
   ```

## Setting Up Node.js (Only for Node based projects)

1. Initialize a new Node.js project:
   ```bash
   npm init -y
   ```
2. Install necessary packages (if any). For example, if you're using a bundler like Webpack or Parcel:
   ```bash
   npm install webpack webpack-cli --save-dev
   ```
   *(Adjust the command based on your bundler or build tool.)*

## Bundling the Project 

1. Set up your build tool according to its documentation.
2. Add a build script in your `package.json`:
   ```json
   "scripts": {
     "build": "webpack" // Replace with your build command
   }
   ```
3. Run the build script:
   ```bash
   npm run build
   ```

## Deploying to Firebase

1. Install Firebase CLI globally (if not already installed):
   ```bash
   npm install -g firebase-tools
   ```
2. Log in to Firebase:
   ```bash
   firebase login
   ```
3. Initialize your Firebase project:
   ```bash
   firebase init
   ```
   - Follow the prompts to set up hosting.
   - When asked for the public directory, enter the build folder name (e.g., `.` for selecting your current folder).
4. Deploy your project:
   ```bash
   firebase deploy
   ```
