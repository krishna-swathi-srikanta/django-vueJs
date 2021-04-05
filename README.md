# django-vueJs
First Django VueJs application

## first-django-app
1. pip install virtualenv 
2. virtualenv venv 
3. activate virtualenv => source venv/bin/activate if mac or linux , venv/script/activate
4. pip install django , pillow  , then pip freeze > requirements.txt
5. check django installed or not and check version with django-admin --version 
6. create django project => django-admin startproject <name of project> 
7. Migrate django models => go inside project root folder , run  python manage.py migrate 
8. Create super user => python manage.py createsuperuser , my credentials , swathi , swathi01
9. run project => python manage.py runserver
10. create new app => python manage.py startapp products
11. Add app in settings.py 
  INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'products',
]
12. Create models Manufacturer and Product , migrate db changes => python manage,py makemigrations , python manage.py migrate

13. create detail and list view in views.py file
14. setup settings.py for static files 
    import os 
    # Add these new lines
    STATICFILES_DIRS = (
        os.path.join(BASE_DIR, 'static'),
    )

    STATIC_ROOT = os.path.join(BASE_DIR, 'staticfiles')
    
15. in project_folder/urls.py
    from django.conf.urls.static import static
    from django.conf import settings
    urlpatterns = [
        path('admin/', admin.site.urls),
        path('',include("products.urls"))
    ]+ static(settings.STATIC_URL, document_root=settings.STATIC_ROOT)


16. create templates/<app_name> folders inside app_folder(products)


## first-django-api


