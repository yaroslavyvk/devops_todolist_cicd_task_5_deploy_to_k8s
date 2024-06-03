# Django ToDo list

This is a todo list web application with basic features of most web apps, i.e., accounts/login, API, and interactive UI. To do this task, you will need:

- CSS | [Skeleton](http://getskeleton.com/)
- JS  | [jQuery](https://jquery.com/)

## Explore

Try it out by installing the requirements (the following commands work only with Python 3.8 and higher, due to Django 4):

```
pip install -r requirements.txt
```

Create a database schema:

```
python manage.py migrate
```

And then start the server (default is <http://localhost:8000>):

```
python manage.py runserver
```

Now you can browse the [API](http://localhost:8000/api/) or start on the [landing page](http://localhost:8000/).

## Task

Extend a GitHub Actions workflow for this project with a Docker build and push to the DockerHub Registry.
Docker CI Job Requirements:

1. Update your forked repository with your DockerHub username and password.
2. Update DockerImageName with your DockerHub image repository name
3. Add `helm-ci` job to the workflow.
4. Repository should be checkedout only once per workflow run
5. New Job should include the following steps:
    1. Download helm artifacts
    1. Execute `helm template` for the chart
    1. Execute `helm lint` for the chart
    1. Package the chart
    1. Upload the chart to the GitHub artifacts
6. Create a Pull Request with the changes.
7. Pull Requests description should also contain a reference to a workflow run with successfull Docker CI job.
