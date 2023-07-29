# Authentication & Production Server
## Reading Questions
1. What is the primary purpose of JSON Web Tokens (JWTs) and how do they work in terms of encoding and decoding data?
   
**Primary Purpose of JSON Web Tokens (JWTs) and How They Work:**
* The primary purpose of JSON Web Tokens (JWTs) is to securely transmit information between parties in a compact and self-contained way. JWTs are commonly used to authenticate users and enable secure communication between a client (typically a web browser or a mobile app) and a server.

* JWTs consist of three parts: header, payload, and signature. Each part is Base64Url-encoded and separated by dots ('.'). The encoding and decoding process works as follows:

**Encoding:** When a user logs in or performs an authentication action, the server creates a JWT by taking the header, payload, and a secret key. The header typically includes the token's type (JWT) and the hashing algorithm used to create the signature 
1. Convert the header and payload into JSON format.
2. Base64Url-encode the JSON header and payload separately.
3. Concatenate the Base64Url-encoded header and payload with a dot ('.') in between.
4. Create the signature by hashing the concatenated header and payload with the secret key using the specified algorithm.
5. Base64Url-encode the signature.
6. Combine the Base64Url-encoded header, payload, and signature with dots ('.') in between to form the JWT.

**Decoding:** When the server receives a JWT from a client, it verifies the authenticity and integrity of the token before processing it.
1. Split the JWT into its three parts by separating with dots ('.').
2. Base64Url-decode the header and payload.
3. Use the header's hashing algorithm and the server's secret key to compute the signature again.
4. Base64Url-encode the recalculated signature.
5. Compare the recalculated signature with the one extracted from the JWT. If they match, the JWT is considered valid and can be trusted.


2. How does JWT Authentication integrate with Django REST Framework to secure API endpoints, and what are the key components involved in this process?
**JWT Authentication with Django REST Framework:**
Django REST Framework (DRF) provides built-in support for JWT authentication through the "djangorestframework-simplejwt" package. Here's a general outline of how JWT authentication integrates with DRF to secure API endpoints:

**Installation:** First, you need to install the "djangorestframework-simplejwt" package in your Django project.

**Configuration:** Configure DRF settings and authentication classes in your project's settings.py file to enable JWT authentication.

**Authentication Flow:** When a user successfully logs in with their credentials, the server generates a JWT for that user. This JWT is sent back to the client, which stores it (usually in local storage or cookies).

**Subsequent Requests:** For each subsequent request to a protected API endpoint, the client must include the JWT in the Authorization header, typically in the form of "Bearer <token>". The server receives the token, verifies its validity, and grants access to the requested resource if the token is valid and not expired.

**Expiration and Refresh Tokens:** JWTs have an expiration time, and once they expire, the user must log in again to get a new token. To avoid frequent logins, DRF supports using refresh tokens. When a JWT expires, the client can use a refresh token (if provided by the server) to get a new JWT without entering their credentials again.

**Key Components:** The key components involved in JWT authentication with DRF are:
  
  1. **Authentication Backend:** A backend responsible for verifying JWTs and authenticating users based on the tokens.

  2. **Authentication Classes:** Configured in DRF settings, these classes determine the authentication method for the API views. In this case, you'd use the JWT authentication class to enable JWT authentication for specific views.

  3. **Views and Endpoints:** You need to define views for handling user login, token refresh, and other authentication-related actions. Additionally, you'll protect specific API endpoints that require authentication by adding the appropriate authentication classes to the view or using DRF's `@authentication_classes` decorator.
     
3. Why is Django’s built-in runserver not suitable for production environments, and what are some alternative server options that should be considered for deploying a Django application?
**Django's built-in runserver and Production Environments:**
Django's built-in development server (`runserver`) is simple to use and convenient for development purposes. However, it's not suitable for production environments for several reasons:

1. **Performance:** The `runserver` is single-threaded and not optimized for handling a large number of concurrent requests. Production-ready servers like Gunicorn or uWSGI can handle multiple requests simultaneously and efficiently.

2. **Security:** The development server lacks some security features needed for production, such as fine-tuned access controls, SSL/TLS support, and other measures to protect against common web vulnerabilities.

3. **Stability and Reliability:** The built-in server is designed for development, and while it automatically reloads when code changes occur, it may not be as stable or reliable as production-grade servers.

4. **Scalability:** The `runserver` is not built to scale and distribute requests across multiple processes or machines. Production servers like Gunicorn or uWSGI can be easily scaled horizontally to handle increased traffic.

5. **Static File Serving:** Production servers are better equipped to efficiently serve static files (CSS, JavaScript, images, etc.) using tools like NGINX or Apache.

* For deploying a Django application in a production environment, it is recommended to use a production-ready web server like Gunicorn or uWSGI. Additionally, it is common to use a reverse proxy server like NGINX or Apache in front of the application server to handle tasks like load balancing, SSL termination, and serving static files. This setup provides better performance, security, and scalability for production use.

## Things I want to know more about
* DRF JWT Authentication
* JSON Web Tokens
