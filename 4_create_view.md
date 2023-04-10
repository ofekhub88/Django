### in app directory view.py

```python
from django.shortcuts import render,get_object_or_404

from django.http import HttpResponse

from .models import Course  # import from Model file

# Create your views here.

def index(request):
    courses = Course.objects
    return render(request, 'courses/index.html',{'courses':courses})  # pass the content of courses table into index.html template

def detail(request,course_id):
    course_detail = get_object_or_404(Course,pk=course_id) # query teh course table with course_id
    return render(request, 'courses/detail.html', {'course':course_detail})
```
