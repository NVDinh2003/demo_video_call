Here is a beautified `README.md` for your Spring Boot with WebRTC project:

```markdown
# Spring Boot with WebRTC

This project demonstrates the use of Spring Boot with WebRTC for real-time communication. Follow the steps below before running the application.

## Steps

### 1. Generate Certificates

You need to generate SSL certificates for secure communication.

- Replace `<YOUR_LOCAL_IP>` with the local IP address of your computer/host. For example:
  ```
YOUR_LOCAL_IP = 192.168.0.166
  ```

- Create an empty `ssl` folder under the project directory:
  ```bash
  mkdir ssl
  ```

- Run the following command to generate the certificates:
  ```bash
  openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout ssl/private_key.pem -out ssl/certificate.pem -subj "//C=US//ST=California//L=San Francisco//O=MyOrganization//OU=MyDepartment//CN=<YOUR_LOCAL_IP>"
  ```

### 2. Update `nginx.conf`

- Open the `nginx.conf` file and replace `<YOUR_LOCAL_IP>` with your local IP (same as in step 1).

### 3. Update `client.js`

- Locate the `client.js` file in the following directory:
  ```
  src/main/resources/static/client.js
  ```

- Update the file to reflect your local configuration.

### 4. Build Docker Image

To run the application with Docker, execute the following command:
```bash
sudo docker-compose up -d --build
```

---

Now, you're all set to run the Spring Boot WebRTC application!
```

This `README.md` format is clean, structured, and easy to follow.