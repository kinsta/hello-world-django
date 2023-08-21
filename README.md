![Photo by Yoksel 🌿 Zok on Unsplash](https://user-images.githubusercontent.com/2342458/202705332-ac5f854f-6622-462d-b5c9-f2f1f0d61b45.png)

# Kinsta - Hello World - Django
An example of how to set your Django application up to enable deployment on Kinsta App Hosting services.

---
Kinsta is a developer-centric cloud host / PaaS. We’re striving to make it easier for you to share your web projects with your users. Focus on coding and building, and we’ll take care of deployment and provide fast, scalable hosting. + 24/7 expert-only support.

- [Start your free trial](https://kinsta.com/signup/?product_type=app-db)
- [Application Hosting](https://kinsta.com/application-hosting)
- [Database Hosting](https://kinsta.com/database-hosting)

## Dependency Management
Django is a Python-based web framework, so during the build process Kinsta will automatically install dependencies 
defined in your `requirements.txt` file.

The `python manage.py collectstatic` command will also be executed at every build to collect all static files to 
the 
directory defined in `STATIC_ROOT`.

## Environment Variables

Note that the `SECRET_KEY` should not be stored in your repository, but rather set up in an environment 
variable. Set a random string in your newly created app's Settings > Environment variables section and make it 
available as both build and runtime variables. Finally, redeploy your application on the Deployments page to 
make the changes effective.

## Web Server Setup

### Start Command
When deploying an application Kinsta will automatically create a processes based on the Procfile in the root of 
the repository. Make sure to use this command to run your server:

```
web: gunicorn helloworld.wsgi
```

## Watch How to Set Up a Django Application on Kinsta
[![Watch the video](https://img.youtube.com/vi/6nbEnnZxisY/maxresdefault.jpg)](https://www.youtube.com/watch?v=6nbEnnZxisY)
