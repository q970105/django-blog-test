#DjangoBlog

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
🌍
*[English](/docs/README-en.md) ∙ [Simplified Chinese](README.md)*

Blog based on `python3.8` and `Django4.0`.

[![Django CI](https://github.com/liangliangyy/DjangoBlog/actions/workflows/django.yml/badge.svg)](https://github.com/liangliangyy/DjangoBlog/actions/workflows/django .yml) [![CodeQL](https://github.com/liangliangyy/DjangoBlog/actions/workflows/codeql-analysis.yml/badge.svg)](https://github.com/liangliangyy/DjangoBlog/actions /workflows/codeql-analysis.yml) [![codecov](https://codecov.io/gh/liangliangyy/DjangoBlog/branch/master/graph/badge.svg)](https://codecov.io/gh /liangliangyy/DjangoBlog) [![license](https://img.shields.io/github/license/liangliangyy/djangoblog.svg)]()

## The main function:
- Add, delete, edit articles, pages, categories, tags, etc. Articles, comments and pages support `Markdown` and code highlighting.
- Support full text search of articles.
- Full commenting functionality, including replying to comments and email reminders for comments, supports `Markdown`.
- Sidebar features, latest articles, most read, tag cloud and more.
- Support Oauth login, there are Google, GitHub, facebook, Weibo, QQ login.
- Support `Redis` cache, support cache automatic refresh.
- Simple SEO functions, new articles, etc. will automatically notify Google and Baidu.
- Integrated simple map bed function.
- Integrate `django-compressor`, automatically compress `css`, `js`.
- Website exception email reminder, if there is an uncaught exception, a reminder email will be automatically sent.
- Integrated WeChat official account function, now you can use WeChat official account to manage your vps.


## Install
The mysql client has been modified from `pymysql` to `mysqlclient`. For details, please refer to [pypi](https://pypi.org/project/mysqlclient/) for preparations before installation.

Install using pip: `pip install -Ur requirements.txt`

If you don't have pip, install it as follows:
- OS X / Linux computer, execute in terminal:

    ````
    curl http://peak.telecommunity.com/dist/ez_setup.py | python
    curl https://bootstrap.pypa.io/get-pip.py | python
    ````

- Windows computers:

    Download http://peak.telecommunity.com/dist/ez_setup.py and https://raw.github.com/pypa/pip/master/contrib/get-pip.py and double-click to run.


## run

 Modify `djangoblog/setting.py` to modify the database configuration as follows:

````python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'djangoblog',
        'USER': 'root',
        'PASSWORD': 'password',
        'HOST': 'host',
        'PORT': 3306,
    }
}
````

### Create database
Execute in mysql database:
```sql
CREATE DATABASE `djangoblog` /*!40100 DEFAULT CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci */;
````

Then execute in the terminal:
```bash
python manage.py makemigrations
python manage.py migrate
````

### Create superuser

 Execute in terminal:
```bash
python manage.py createsuperuser
````

### Create test data
Execute in terminal:
```bash
python manage.py create_testdata
````

### Collect static files
Execute under the terminal:
```bash
python manage.py collectstatic --noinput
python manage.py compress --force
````

### start operation:
Execute: `python manage.py runserver`


Open the browser: http://127.0.0.1:8000/ to see the effect.

## server deployment

For local installation and deployment, please refer to [DjangoBlog Deployment Tutorial](https://www.lylinux.net/article/2019/8/5/58.html)
There are detailed deployment introductions.

This project already supports the use of docker for deployment. If you have a docker environment, you can use docker to deploy. For details, please refer to: [docker deployment](/docs/docker.md)



## More configuration:
[More configuration introduction](/docs/config.md)
[Integrated elasticsearch](/docs/es.md)

## Question related

If you have any questions, please submit an Issue, or send the problem description to my email `liangliangyy#gmail.com`. I will answer as soon as possible. It is recommended to submit an Issue.

---
 ## To everyone 🙋‍♀️🙋‍♂️
 If this project helps you, please leave your URL [here](https://github.com/liangliangyy/DjangoBlog/issues/214) so ​​that more people can see it.
Your reply will be the motivation for me to continue to update and maintain.


## Donate
If you think this project is helpful to you, you are welcome to invite me for a cup of coffee. Your support is my greatest motivation. You can scan the QR code below to pay for me, thank you.
### Alipay:
<div>
<img src="https://resource.lylinux.net/image/2017/12/16/IMG_0207.jpg" width="150" height="150" />
</div>

### WeChat:
<div>
<img src="https://resource.lylinux.net/image/2017/12/16/IMG_0206.jpg" width="150" height="150" />
</div>

---

thanks jetbrains
<div>
<a href="https://www.jetbrains.com/?from=DjangoBlog"><img src="https://resource.lylinux.net/image/2020/07/01/logo.png" width= "150" height="150"></a>
</div>
