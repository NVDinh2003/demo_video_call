# Spring Boot with WebRTC

This README provides instructions for setting up and running the Spring Boot WebRTC application.

## Prerequisites

Before running the application, follow these steps:

### 1. Generate Certificates

First, determine your local IP address. For example: `YOUR_LOCAL_IP = 192.168.0.166`

Create an empty `ssl` folder in the project directory and generate the certificates:

```bash
mkdir ssl && openssl req -x509 -nodes -days 365 -newkey rsa:2048 \
-keyout ssl/private_key.pem -out ssl/certificate.pem \
-subj "//C=US//ST=California//L=San Francisco//O=MyOrganization//OU=MyDepartment//CN=<YOUR_LOCAL_IP>"
```

Replace `<YOUR_LOCAL_IP>` with your actual local IP address.

### 2. Update nginx.conf

In the `nginx.conf` file, replace `<YOUR_LOCAL_IP>` with your local IP address (the same one used in step 1).

### 3. Update client.js

Navigate to `src/main/resources/static/client.js` and make any necessary updates.

### 4. Build Docker Image

Run the following command to build and start the Docker containers:

```bash
sudo docker-compose up -d --build
```

## Running the Application

After completing the above steps, your Spring Boot WebRTC application should be ready to run.

For additional information or troubleshooting, please refer to the project documentation or contact the development team.