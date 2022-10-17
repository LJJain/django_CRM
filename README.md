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

## 參考資料

> 解決無法開啟 django-admin 教學:
- https://www.youtube.com/watch?v=ezSGmWk9KA0&ab_channel=urpointofview


## Github

> git 位置:
- git remote add origin https://github.com/LJJain/django_CRM.git
