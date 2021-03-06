# Installation and Deployment
Take a look at `DEPLOY.bash`.
On Debian-like system, try:
> bash -c "$(curl https://raw.githubusercontent.com/Babaritech/babar3/master/DEPLOY.bash)"

Don't forget to read the [Django checklist](https://docs.djangoproject.com/en/1.9/howto/deployment/checklist/).
You cant get SSL certificates with [letsencrypt](https://github.com/letsencrypt/letsencrypt).


## Development
Both Django and Angular get a special dev server.
They are available with:
```bash
cd back
source ./env/bin/activate
python3 manage.py runserver
```

```bash
cd front
grunt serve
```


# Migration
To migrate the old babar database to the new one:
- First get a JSON dump of the old DB
- Convert it with `migrate.py old.json`
- Import it in Django `python3 manage.py loaddata new.json`


# API documentation
Available at `/docs/`.


# Relevant ressources
## Back
- [Django](https://www.djangoproject.com/)
- [Django REST framework](http://www.django-rest-framework.org/)
- [Django REST auth](https://django-rest-auth.readthedocs.org)

## Front
- [Yeoman: generator-angular](https://github.com/yeoman/generator-angular)
- [Angular](https://docs.angularjs.org/)
- [Angular Material Design](https://material.angularjs.org/latest/)
