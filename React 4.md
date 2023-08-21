# React 4

## Reading Questions

1. Explain the concept of dynamic routes in Next.js and how they differ from static routes.
Dynamic Routes vs. Static Routes in Next.js:

* In Next.js, dynamic routes allow you to create pages with URLs that can vary based on parameters. They enable you to generate pages for multiple routes without having to create a separate page for each variation. Dynamic routes are defined using brackets [] within the page filename. For example, if you have a dynamic route named post, you could create a file called [post].js to handle URLs like /post/1, /post/2, and so on.

* Static routes, on the other hand, are created by placing individual files in the pages directory. Each file in the pages directory corresponds to a specific route. Static routes are pre-built at build time and don't have parameters that change dynamically.

2. Describe the process of deploying a Next.js application. What are the key steps involved, and what are some deployment platforms you can use?

* Deploying a Next.js application involves several steps:

 1. Build the Application: Run the build command, typically npm run build or yarn build, which generates an optimized production build of your application.

 2. Choose a Deployment Platform: There are several platforms you can use to deploy a Next.js application, including:

  * Vercel: Designed for Next.js applications, it offers easy integration and automatic deployments based on Git repositories.
  * Netlify: A popular platform that supports static site deployment and can be used for Next.js apps as well.
  * AWS Amplify: Provides a streamlined way to deploy and manage web applications, including Next.js projects.
  * DigitalOcean: Offers scalable infrastructure for deploying various types of applications, including Next.js apps.
  
 3. Configure Deployment Settings: Each platform will have its own setup process. Generally, you'll need to connect your repository, specify the build command, and set environment variables if needed.

 4. Deploy: Once configured, trigger the deployment process. The platform will build your application, optimize assets, and make it accessible online.

 5. Domain Configuration: After deployment, you can configure a custom domain name for your application if desired.

 6. SSL Certificate: Many platforms provide automatic SSL certificates to ensure secure connections to your application.

3. How does Next.js handle static file serving? Discuss the default folder structure for storing static assets and explain how to reference them in a Next.js application.
 

* Next.js handles static file serving through the public directory. The default folder structure for static assets is as follows:
 """
 project-root/
  └── public/
      └── images/
      └── styles/
      └── ...
  └── pages/
  └── ...
 """
 * To reference static assets in your Next.js application, you can use the /public URL prefix. For example, if you have an image named logo.png in the public/images directory, you can reference it in your code like this:

   """
     <img src="/images/logo.png" alt="Logo" />
     Next.js automatically handles these static assets and optimizes them for production during the build process.
   """
 * Remember that while Next.js is optimized for server-rendered applications, it also supports client-side rendering and hybrid rendering, offering flexibility in how you structure and serve your content.

## Things I want to know more about
* Dynamic Routes
* Deployment
