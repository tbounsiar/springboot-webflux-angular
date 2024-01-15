# Spring Boot WebFlux and Angular Web Application Example

This repository contains a simple example of a web application built using Spring Boot WebFlux as the backend and Angular as the frontend. The application showcases the integration of these technologies to create a modern, reactive web application.

### How to Run

1. Ensure you have node, Java and Maven installed.
2. navigate to the `front` directory and run the following commands.
   ```bash
   npm install
   npm run watch
   ```
   This will build a distribution to `front/dist/front/browser`
3. Navigate to the `backend` directory.
   1. Create Symbolic Link to `front/dist/front/browser`
   
      Using cmd as admin in Windows
      ```shell
      mklink /D src/main/resources/public ../front/dist/front/browser
      ```
      Using PowerShell in Windows
      ```shell
      New-Item -ItemType SymbolicLink -Path src/main/resources/public -Target ../front/dist/front/browser
      ```
      Linux
      ```shell
      mklink src/main/resources/public ../front/dist/front/browser
      ```
   2. Run the following command to build and start the backend server:
      ```bash
      mvn spring-boot:run
      ```