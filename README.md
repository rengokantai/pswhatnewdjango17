#### pswhatnewdjango17
#####migrations
```
makemigrations //then
migrate
```
######moving back and forth
```
manage.py migrate appname 0001
manage.py migrate appname zero     //unapply all
```
######complex example
add a non-nullable column in a table.
when
```
manage.py makemigrations
```
it will have two options. 1 provide one-off default 2 quit  
for complex senario use sqlmigrate
```
manage.py sqlmigrate appname 0003
```
#####add loading
```
manage.py shell
```
```
>>> from django.apps import apps
>>> apps.get_app_configs()
>>> apps.get_app_config('appname').name
```

#####models and other changes
######The new system check
```
python manage.py check
```
check model syntax error
#####misc
######secu middleware
```
MIDDLEWARE_CLASSES =('django.middleware.security.SecurityMiddleware',)
```
######TestCase
```
TestCase.setUpTestData()
```
