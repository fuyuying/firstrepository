# repository 1

1.MydjangoProject/MydjangoProject/settings.py:

INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'HelloWorld',
]



2.MydjangoProject/HelloWorld/views.py:

#coding:utf-8
from django.shortcuts import render
#from django.http import HttpResponse
def index(request):
       #return HttpResponse(u"Hello World! ´ó¼ÒºÃ£¡")
       return render (request,"index.html",)


3.MydjangoProject/MydjangoProject/urls.py:

from django.contrib import admin
from django.urls import path
from HelloWorld import views as HelloWorld_views

urlpatterns = [
    path('',HelloWorld_views.index),   
    path('admin/', admin.site.urls),
]
