# Spring Boot Basic Authentication Example 🔐

This is a simple demonstration project showcasing how to implement basic authentication for a REST API using **Spring Boot** and **Spring Security**. The application exposes a single secured endpoint, and access credentials are configured in the `application.properties` file.

## Features ✨

* **Secured REST Endpoint**: A single `/welcome` endpoint is protected.
* **Basic Authentication**: Utilizes Spring Security's default basic authentication mechanism.
* **Externalized Configuration**: Username and password can be easily changed in the `application.properties` file.

***

## Technologies Used 🛠️

* **Java 17**
* **Spring Boot 3.x**
* **Spring Security**
* **Spring Web**
* **Maven**

***

## Getting Started 🚀

Follow these instructions to get a copy of the project up and running on your local machine.

### Prerequisites

Make sure you have the following software installed:
* **JDK 17** or newer
* **Apache Maven**

### Installation & Running

1.  **Clone the repository**
    ```bash
    git clone <your-github-repository-url>
    ```

2.  **Navigate to the project directory**
    ```bash
    cd <project-folder-name>
    ```

3.  **Run the application using the Maven wrapper**
    * On macOS/Linux:
        ```bash
        ./mvnw spring-boot:run
        ```
    * On Windows:
        ```bash
        mvnw.cmd spring-boot:run
        ```

The application will start on the default Tomcat port `8080`.

***

## How to Test the API

The application has one secured endpoint. You must provide the correct credentials to access it.

* **URL**: `http://localhost:8080/rest/auth/welcome`
* **Default Username**: `admin`
* **Default Password**: `geeksforgeeks`

### Using a Web Browser

Navigate to the URL in your browser. A login pop-up will appear, prompting you for a username and password.



### Using cURL

You can also test the endpoint from your command line using a tool like `cURL`.

```bash
curl -u admin:geeksforgeeks http://localhost:8080/rest/auth/welcome


Successful Response:

Hey! welcome to GeeksforGeeks
Failed Response (Incorrect Credentials): You will receive a 401 Unauthorized error.

Configuration
You can easily change the login credentials by editing the src/main/resources/application.properties file.

Properties

# Default security credentials
spring.security.user.name=your-new-username
spring.security.user.password=your-new-password

if this steps followed thoroughly the file working will be done smoothly

but must ensure the required installations priority.
