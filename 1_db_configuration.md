# in setting.py in the prpoject level

```yaml
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        #'NAME': os.path.join(BASE_DIR, 'db.sqlite3'),
        'NAME': 'portfoliodb',
        'USER': 'postgres',
        'PASSWORD': 'your passord',
        'HOST':'localhost',
        'PORT': '5432',

    }
}
```
