# streetworkout

### dev
* the devcontainer configuration was referenced from [here](https://github.com/microsoft/vscode-dev-containers/tree/v0.109.0/containers/python-3-postgres)

* boot app server 
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