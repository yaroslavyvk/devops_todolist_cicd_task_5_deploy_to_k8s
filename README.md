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
    1. Add Corresponding secrets to the repository.
2. Update DockerImageName with your DockerHub image repository name
3. Add a resubable workflow to deploy to `kind` kubernetes cluster.
    1. Reusable workflow should allow to deploy to different `environemnts`
    1. Add steps to spin up a `kind` cluster from a `cluster.yml` file.
    1. Job should contain a step with `helm install --dry-run` command.
    1. Job should containe a step to run `helm upgrade --install` command. This command should be `atomic` and should not allow to deploy a broken release.
    1. All secrets should be stored in the environment secrets.
4. Call reusable workflow to deploy to `development` environment.
5. Call reusable workflow to deploy to `staging` environment.
6. Create a Pull Request with the changes.
7. Pull Requests description should also contain a reference to a workflow run with successfull Docker CI job.
