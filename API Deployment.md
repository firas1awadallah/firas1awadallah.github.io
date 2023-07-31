# API Deployment
## Reading Questions
1. What are the key principles to follow when organizing and configuring Django settings for a project, according to the “Django Settings Best Practices” reading?
   
**Key Principles for Django Settings Organization**:
When organizing and configuring Django settings for a project, some best practices include:
   - **Separation of Concerns**: Divide settings into different files for different purposes, such as base settings, development settings, production settings, etc.
   - **Environment-based Configuration**: Use environment variables to set sensitive information like secret keys, database credentials, etc., and keep them out of version control.
   - **Use Settings Packages**: Utilize settings packages like `django-configurations` to make settings management more flexible and modular.
   - **Consistency and Readability**: Maintain a consistent structure and naming convention for settings to make them more readable and understandable.
   - **Use Defaults**: Provide default values for settings whenever possible to avoid errors and simplify configuration for developers.
   - **Secrets Protection**: Keep sensitive information secure by using tools like `python-decouple` to store them externally.
   - **Version Control**: Avoid committing environment-specific settings and sensitive information to version control.
2. How does the White Noise library contribute to the efficient serving of static files in a Django application, and what are the steps to integrate it into a project?

 **White Noise for Efficient Serving of Static Files in Django**:
Django is not the most efficient way to serve static files directly in production, especially in high-traffic scenarios. WhiteNoise is a Python library that allows Django to serve static files efficiently, improving performance and reducing the need for additional server configuration.

Integration Steps for WhiteNoise:
   - First, install the WhiteNoise library: `pip install whitenoise`.
   - In your Django project's settings, add `'whitenoise.middleware.WhiteNoiseMiddleware'` to the `MIDDLEWARE` setting. Place it before `django.middleware.security.SecurityMiddleware`.
   - Remove the `django.contrib.staticfiles` app from `INSTALLED_APPS`, as WhiteNoise takes over static file handling.
   - Configure your web server to disable its own static file handling, as WhiteNoise will handle it.
3. What is the purpose of Cross-Origin Resource Sharing (CORS) in web applications, and how can it be implemented and configured in a Django project to control access to resources?

**Cross-Origin Resource Sharing (CORS) in Django**:
CORS is a security feature implemented by web browsers to control access to resources (e.g., APIs) served from different domains. It prevents web pages from making requests to a different domain than the one that served the web page.

To implement and configure CORS in a Django project, you can use the `django-cors-headers` package, which simplifies the process. Here's how to do it:

   - Install the `django-cors-headers` package: `pip install django-cors-headers`.
   - Add `'corsheaders'` to your `INSTALLED_APPS` in the Django settings.
   - Configure the middleware by adding `'corsheaders.middleware.CorsMiddleware'` to the `MIDDLEWARE` setting. Place it above `django.middleware.common.CommonMiddleware`.
   - Define the origins that are allowed to access your resources using the `CORS_ORIGIN_WHITELIST` setting.
   - Configure other CORS settings such as `CORS_ALLOW_METHODS`, `CORS_ALLOW_HEADERS`, etc., as per your project requirements.
## Things I want to know more about
* Django Settings Best Practices
* White Noise library
* purpose of Cross-Origin Resource Sharing (CORS)
