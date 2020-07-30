# streetworkout

## Purpose
* This is a try out project for Django framework and VSCode (WSL2 + Docker Desktop) development strategy. 

### To develop
* the devcontainer configuration was referenced from [here](https://github.com/microsoft/vscode-dev-containers/tree/v0.109.0/containers/python-3-postgres)

* boot app server (from within the container)
```bash
cd mysite
python manage.py runserver 0:8000
```

* to copy the template file from the local site-package
```bash
python -c "import django; print(django.__path__)"

vscode@7e598c0e8e7f:/workspace/mysite$ cp /usr/local/lib/python3.8/site-packages/django/contrib/admin/templates/admin/base_site.html templates/admin/

vscode@7e598c0e8e7f:/workspace/mysite$ cp /usr/local/lib/python3.8/site-packages/django/contrib/admin/templates/admin/index.html templates/admin/
```

### pass the git credential into container
* ssh key from WSL2 Ubuntu (failed!)




### how to create admin user
* [here](https://docs.djangoproject.com/en/3.0/intro/tutorial02/#introducing-the-django-admin)

* test credential 

### Configure global options with .wslconfig
* [here](https://docs.microsoft.com/en-us/windows/wsl/wsl-config#configure-global-options-with-wslconfig)

### Dockerfile
* beware that the Dockerfile for development and production should be different.
* consider using Multi-stage builds for production image to greatly minimized the image size. [ref](https://www.docker.com/blog/containerized-python-development-part-1/)
* while for developement, you might need those extra tools, e.g. pip, reside inside the image. 


