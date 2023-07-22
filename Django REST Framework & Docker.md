## Reading Questions
1. What are the key components of a Docker container, and how do they help streamline the development and deployment of applications?
* Key components of a Docker container and their benefits:
Docker is a platform that allows developers to package applications and their dependencies into lightweight containers, which can be run consistently on any environment that supports Docker. The key components of a Docker container are:

a. Docker Image: A Docker image is a read-only template that contains the application code, runtime, libraries, and dependencies needed to run the application. It is the building block of Docker containers. Images are versioned and can be stored in Docker repositories, making it easy to distribute and share applications.

b. Docker Container: A Docker container is an instance of a Docker image. It encapsulates the application and its environment in an isolated and portable runtime. Containers are lightweight, fast to start and stop, and share the host operating system's kernel, reducing resource overhead compared to traditional virtual machines.

c. Dockerfile: The Dockerfile is a text file that defines the steps and instructions to build a Docker image. It specifies the base image, the application code to be copied, the environment variables, and other configurations needed for the image.

d. Docker Registry: The Docker registry is a centralized repository that stores Docker images. The default registry is Docker Hub, but private registries can be set up for secure image storage.

* Benefits of Docker for development and deployment of applications:

a. Consistency: Docker ensures that the application runs consistently across different environments, such as development, staging, and production, eliminating the "it works on my machine" problem.

b. Isolation: Containers isolate the application and its dependencies, reducing conflicts and providing a clean environment for each application.

c. Portability: Docker containers can run on any system that supports Docker, making it easier to move applications between different hosts and cloud platforms.

d. Resource Efficiency: Docker containers share the host OS kernel, resulting in lower resource overhead compared to traditional virtual machines.

e. Version Control: Docker images can be versioned and tagged, allowing easy rollback or updating to specific application versions.

f. Scalability: Docker containers can be scaled horizontally to handle increased workloads by running multiple instances of the same container.

2. Describe the primary steps involved in building a library website using Django, including essential components like models, views, and templates.

* Building a library website using Django:

Step 1: Set up the Django project and application.
Install Django using pip: pip install django
Create a new Django project: django-admin startproject library_project
Create a new Django application within the project: python manage.py startapp library_app

Step 2: Define models.
In the models.py file of the library_app, define the models representing the data entities, such as Book, Author, and Genre. For example:

Step 3: Create and apply migrations.
Generate the initial migration for the models: python manage.py makemigrations
Apply the migrations to create the database tables: python manage.py migrate

Step 4: Create views and templates.
In the views.py file of the library_app, define views that handle HTTP requests and interact with the models.

Step 5: Configure URLs.
In the urls.py file of the library_app, define URL patterns to map views to URLs.

Step 6: Run the development server.
Start the Django development server: python manage.py runserver
Visit link in your web browser .

3. Can you explain the primary differences between Django and Django REST framework?

* Differences between Django and Django REST framework:
Django is a powerful web framework for building web applications, while Django REST framework (DRF) is an extension to Django that simplifies the creation of RESTful APIs. Here are the primary differences between them:

* Purpose:
Django: Designed for building full-stack web applications, handling backend logic, database models, views, and templates.
Django REST framework: Focused on building APIs, providing tools and serializers to work with API data formats like JSON, XML, etc.

* Serializers:
Django: Django uses form classes to handle incoming data from HTML forms.
Django REST framework: DRF introduces serializers that allow easy conversion between complex data types like Django models and Python data types and render data in different formats for API responses.

* Views:
Django: Views in Django handle HTTP requests and return HTTP responses, typically for rendering HTML pages.
Django REST framework: DRF views are tailored for API responses, handling serialization, content negotiation, and status codes for API requests and responses.

* Routing:
Django: URL routing in Django is designed for handling HTML-based views and templates.
Django REST framework: DRF provides more robust and flexible routing options, explicitly geared towards API endpoints and HTTP methods.

*Authentication and Permissions:
Django: Authentication and permissions are available for web application views, but not explicitly geared towards APIs.
Django REST framework: DRF provides built-in authentication classes and permissions for securing API endpoints.

* Response Formats:
Django: Typically used for rendering HTML responses.
Django REST framework: Primarily focused on providing JSON and other data formats for API responses.


## Things I want to know more about
* Docker 
* building a library website using Django
* Django REST framework
