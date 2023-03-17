# Vue.js and Spring Boot and SQL Serve

This is a simple example of how to build a web application using Vue.js and Spring Boot.

## Building and Running the Application

To build and run the Spring Boot application, follow these steps:

1. Open a command prompt and navigate to the root directory of the project.
2. Run the following command to build the project:

    ```
    mvn clean install
    ```

3. Once the build is complete, run the following command to start the Spring Boot application:

    ```
    mvn spring-boot:run
    ```

4. The application will be available at http://localhost:8080.

To create a Vue.js component that interacts with the Spring Boot API using axios, follow these steps:

1. Create a new Vue.js component in the `src/components` directory.
2. In the component's `mounted()` method, use Axios to make a GET request to the Spring Boot API:

    ```javascript
    axios.get('/api/users')
      .then(response => {
        // Handle the response
      })
      .catch(error => {
        // Handle the error
      });
    ```

3. Use the response data to populate the component's state and render the data in the component's template.

To build the Vue.js project, follow these steps:

1. Open a command prompt and navigate to the `client` directory.
2. Run the following command to build the project:

    ```
    npm run build
    ```

3. Once the build is complete, copy the built files from the `client/dist` directory to the `src/main/resources/static` directory of the Spring Boot project:

    ```
    cp -R dist/* ../src/main/resources/static/
    ```

4. The Vue.js component will be available at http://localhost:8080.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for
