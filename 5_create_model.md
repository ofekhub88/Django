## in the app directory level you have the models.py file


```python
from django.db import models

# Create your models here.

class Course(models.Model):
    image = models.ImageField(upload_to='images/')
    summary = models.CharField(max_length=200)


    def __str__(self):
        return self.summary
```

## Activate model
```bash
python  manage.py  makemigrations < app name>
python  manage.py  migrate 
```


## Create Model from database existing table
```bash
 python manage.py inspectdb >models.py
```
