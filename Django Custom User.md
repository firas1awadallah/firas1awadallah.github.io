## Reading Questions

1. What are the key benefits of using a Django Custom User Model, and how does it differ from the default Django User Model?
Using a Django Custom User Model offers several benefits compared to the default Django User Model:

* Flexibility: With a Custom User Model, you have full control over the fields and behavior of the user model. You can add, remove, or modify fields according to your project's specific requirements.

* Scalability: The default Django User Model includes several fields that may not be necessary for your application. By creating a Custom User Model, you can optimize the user model to fit your project's needs, potentially improving performance and reducing unnecessary data storage.

* Seamless integration: A Custom User Model allows you to integrate additional authentication methods, such as email-based authentication, or incorporate third-party authentication providers like OAuth or social login.

* Better security: By customizing the user model, you can enhance security measures to suit your application. For example, you can implement password policies, two-factor authentication, or account activation workflows.
  
2. Explain the process of creating and implementing a Custom User Model in Django, including the necessary changes to settings.py and the required model fields.
   
* Start a new Django project
* In your project's directory, create a new app
* Inside the app directory , create a new file called models.py or open it if it already exists.
* Import the necessary modules:
* Create a class for your Custom User Model by subclassing AbstractUser:
* Open your project's settings.py file and find the AUTH_USER_MODEL setting.
* Run the following command to create and apply migrations:
  
3. What is DjangoX and how does it complement or extend the functionality of Django? Provide an example use case for incorporating DjangoX in a project.

DjangoX,  Django itself is highly extensible, and there are many third-party libraries and packages available that complement or extend its functionality.

One such library is Django REST framework (DRF), which is commonly used to build APIs in Django projects. DRF provides additional features for API development, including serializers, authentication, permissions, and more. It complements Django by simplifying the process of creating robust and scalable APIs.

Example use case: Let's say you're building a web application with Django that requires a RESTful API to interact with external clients. By incorporating Django REST framework (DRF) into your project, you can easily serialize your models, define API views, handle authentication and permissions, and provide a standardized API interface. DRF streamlines the API development process, saving you time and effort while ensuring best practices for building APIs with Django.
## Things I want to know more about
* Django Custom User Model
* DjangoX
