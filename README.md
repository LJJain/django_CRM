# Django 練習 CRM

## 日誌
> 2022.10.10
- 開始專案 CRM
- 建立虛擬環境
- 執行app(account)
- 建立分頁 views urls
- 建立獨立urls

> 2022.10.17
- html模板繼承
- 利用Bootstrap建立模板

> 2022.10.19
- static:靜態資料夾 (CSS、JS、Images)
- 建立資料庫 & 超級使用者

> 2022.10.22
- 資料庫查詢&渲染網頁
- 分頁連結 urls.py:name=""->用name做呼叫{% url 'home' %}
- 建立表單
- 站內搜尋功能
- 會員註冊/登入功能



## 筆記
> 安裝虛擬環境
- 安裝:pip install virtualenv
- 開啟:python -m venv (env name)
- 執行:env\Scripts\activate
- 解決 env 無法開啟:系統管理員身分開啟 powershell -> set-executionpolicy remotesigned

> 開始專案
- 開始:django-admin startproject (project name)
- 新增 app:python manage.py startapp (app name)

> 建立獨立urls
- project/urls.py:path('', include('apps.urls')),
- app/urls.py:from . import views -> path('', views.home, name='home'),

> Bootstrap
- html:https://getbootstrap.com/docs/4.0/components/navbar/
- CSS:https://getbootstrap.com/docs/4.0/getting-started/introduction/

> 靜態資料夾
- settings:

    - import os

    - STATICFILES_DIRS = [
        os.path.join(BASE_DIR, 'static'),
    ]

    MEDIA_URL = 'images/' 

- html:{% load static %}  

    - < link rel="stylesheet" type="text/css" href="{% static '/css/main.css' %}" >

> 資料庫建立
- 啟動同步:python manage.py migrate
- 修改/更新資料庫:python manage.py makemigrations (每次新增/更新時都要做一次)
- 建立超級使用者:python manage.py createsuperuser
- 註冊資料庫:admin.py

    - from .models import *

    - admin.site.register(classname)

> 資料庫查詢
- 變數:ModelName.ModelObjects.Method() -> all(),get(),filter(),exclude()

> 客戶獨立頁面
- 變更urls.py:

    path('customer/<str:pk_test>/', views.customer),

> 建立表單
- 建立form.py檔案:

    - from django.forms import ModelForm

> 站內搜尋功能
- 安裝:pip install django-filter
- settings.py:INSTALLED_APPS=['django_filters']
- 新增filters.py

> 註冊&登入
- django內建註冊表單:

    - from django.contrib.auth.forms import UserCreationForm






## 參考資料

> 解決無法開啟 django-admin 教學:
- https://www.youtube.com/watch?v=ezSGmWk9KA0&ab_channel=urpointofview


## Github

> git 位置:
- git remote add origin https://github.com/LJJain/django_CRM.git
