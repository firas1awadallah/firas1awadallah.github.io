# Permissions & Postgresql

## Reading Questions
1. What are the key components and purpose of Django Rest Framework (DRF) permissions, and how do they help in securing an API?
* Django Rest Framework (DRF) Permissions:
DRF provides a flexible permissions system that helps in securing APIs by controlling access to different resources based on user roles and permissions. The key components of DRF permissions are:
- Authentication: DRF allows you to configure various authentication methods, such as session authentication, token authentication, or OAuth, to ensure that only authenticated users can access the API.
- Permissions: DRF includes several built-in permission classes that determine whether a user has the necessary rights to perform specific actions on a resource (e.g., view, create, update, delete). Some common built-in permission classes are:
  - IsAuthenticated: Ensures that the user is authenticated before granting access.
  - IsAdminUser: Restricts access to only admin users.
  - AllowAny: Allows unrestricted access to any user (no authentication required).
  - IsAuthenticatedOrReadOnly: Allows authenticated users to perform write actions (create, update, delete) and unrestricted access (read) for unauthenticated users.
- Custom Permissions: Besides built-in permissions, DRF allows you to create custom permission classes tailored to your application's specific requirements. These custom permissions can control access based on various factors, like user attributes or group memberships.
- Object-level permissions: DRF supports object-level permissions, which allow fine-grained control over individual resources. This ensures that users can only access or manipulate resources they own or have permission to modify.
By using DRF permissions, you can implement a robust security layer for your API, ensuring that sensitive actions and data are only accessible by authorized users or groups.

2. In SQL, what is the purpose of the SELECT statement, and how would you use it to retrieve all columns from a table called ‘employees’?

* Purpose of the SELECT statement in SQL:
In SQL (Structured Query Language), the SELECT statement is used to retrieve data from a database table. It is one of the most fundamental and commonly used SQL commands. The purpose of the SELECT statement is to query and fetch specific data that matches certain conditions.

* The asterisk (*) is a wildcard that represents "all columns." When you execute this SQL statement, the database will return all rows from the 'employees' table, along with all the columns associated with each row.

3. Can you explain the role of DRF Generic Views and provide examples of their usage in building a RESTful API?

* DRF Generic Views and their role in building a RESTful API:
DRF Generic Views are pre-built views provided by Django Rest Framework that simplify the process of building RESTful APIs. They encapsulate common patterns and actions, reducing boilerplate code and promoting code reusability. Generic Views handle common HTTP methods (GET, POST, PUT, DELETE) for different resources in a standard way.

* DRF offers several types of Generic Views:
- `APIView`: The base class for all DRF views. It provides the basic structure and functionality of views, but you need to handle the HTTP methods explicitly.
- `ListAPIView`: Represents a read-only view for listing a queryset. It is similar to the traditional Django ListView.
- `CreateAPIView`: Handles creating new objects based on the provided data in the request.
- `RetrieveAPIView`: Used to retrieve a single object from the database by its primary key.
- `UpdateAPIView`: Allows updating an existing object based on its primary key.
- `DestroyAPIView`: Handles the deletion of an object based on its primary key.
- `ListCreateAPIView`: Combines the functionality of `ListAPIView` and `CreateAPIView`, supporting both listing and creation of objects.
- `RetrieveUpdateDestroyAPIView`: Combines the functionality of `RetrieveAPIView`, `UpdateAPIView`, and `DestroyAPIView`, supporting retrieval, updating, and deletion of a single object.

## Things I want to know more about
* DRF Permissions
* SQL Prework
* Django REST
