# Vulnerable Node.js Application

This is a vulnerable Node.js application created for testing Static Application Security Testing (SAST) tools. The application includes several common vulnerabilities such as XSS, command injection, and insecure logging.

## Project Structure

vulnerable-node-app/
├── Dockerfile
├── docker-compose.yml
├── app.js
├── package.json
├── views/
│ ├── index.html
│ ├── about.html
│ ├── contact.html
│ ├── admin.html
│ └── style.css
└── README.md



## Getting Started

### Prerequisites

- Docker
- Docker Compose

### Running the Application

1. **Build the Docker image**:
    ```sh
    docker-compose build
    ```

2. **Start the application**:
    ```sh
    docker-compose up
    ```

The application will be available at `http://localhost:3000`.

### Stopping the Application

To stop the application, press `Ctrl+C` in the terminal where Docker Compose is running and then remove the containers:
```sh
docker-compose down




Vulnerabilities
Exposing Sensitive Information: The login route logs the username and password to the console.
Reflected XSS: The search route injects the user input directly into the HTML response.
Insecure Logging: The contact form logs sensitive information (email) to the server-side logs.
Command Injection: The admin command execution uses eval() to execute commands, leading to possible command injection.
Disclaimer
This application is intended for educational purposes only. Do not deploy this application in a production environment.



### Criação do Arquivo Zip

Agora vamos criar e salvar os arquivos em um arquivo zip. &#8203;:citation[oaicite:0]{index=0}&#8203;




