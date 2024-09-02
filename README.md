# Email Microservice
## Uber Backend Challenge

![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/spring-%236DB33F.svg?style=for-the-badge&logo=spring&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white)
[![Licence](https://img.shields.io/github/license/Ileriayo/markdown-badges?style=for-the-badge)](./LICENSE)

This project is an API built using **Java**, **Spring Boot**, and **AWS Simple Email Service (SES)**. It was developed to demonstrate how to solve the [Uber Backend Challenge](https://github.com/uber-archive/coding-challenge-tools/blob/master/coding_challenge.md).

## Table of Contents

- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Database](#database)
- [Contributing](#contributing)

## Installation

1. **Clone the repository:**

    ```bash
    git clone https://github.com/Talesztre/desafio-backend-uber.git
    cd desafio-backend-uber
    ```

2. **Install dependencies:**

    Use Maven to install the required dependencies.

    ```bash
    mvn clean install
    ```

3. **Update `application.properties`:**

    Replace the placeholders with your actual AWS credentials:

    ```properties
    aws.region=us-east-1
    aws.accessKeyId=YOUR_ACCESS_KEY_ID
    aws.secretKey=YOUR_SECRET_KEY
    ```

## Configuration

Before running the application, ensure that you have configured the following:

- **AWS SES**: Set up an AWS SES account and verify the sender email address.
- **Environment Variables**: Ensure the AWS credentials and region are correctly set in the `application.properties` file or as environment variables.

## Usage

1. **Start the application:**

    You can start the application using Maven:

    ```bash
    mvn spring-boot:run
    ```

2. **Access the API:**

    The API will be accessible at [http://localhost:8080](http://localhost:8080).

## API Endpoints

The API provides the following endpoints:

### Send an Email

**POST** `/api/email/send` - Sends an email from your sender to the destination.

**Request Body:**

```json
{
  "to": "recipient@example.com",
  "subject": "Your Subject",
  "body": "Your email body here"
}


Response:

200 OK: If the email is successfully sent.
400 Bad Request: If the request payload is invalid.
500 Internal Server Error: If there's an error while sending the email.

Database
This microservice doesn't persist any data in a database as it is focused on sending emails through AWS SES. However, if required, you could integrate
a database like MySQL or PostgreSQL and persist email logs or metadata.

Contributing
Contributions are welcome! If you find any issues or have suggestions for improvements, please feel free to open an issue or submit a pull request to the repository.

When contributing to this project, please follow these guidelines:

Maintain the existing code style.
Use conventional commits for commit messages.
Make changes in a separate branch and submit a pull request for review.

Thank you for your interest in improving this project!



