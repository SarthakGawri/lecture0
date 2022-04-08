# MindConsult
Final Project For [CS50's Web Programming with Python 🐍 and JavaScript](https://cs50.harvard.edu/web).

Big Thanks and A round of applause 👏 to all the course staff and grading team. Thanks to the Discord community as well.

## About Mindconsult
Mindconsult is a mental health consultation web application made using Django, Django channels, JavaScript, HTML, CSS.

This application contains 2 django apps users and consultation.

Users app handles user registration and authentication for consultants and patients using Django's default authentication system customized according to the project.

Consultation app handles the live chat consultation between patients and consultants using Django Channels, Redis and JavaScript WebSocket API.

## Distinctiveness and Complexity

This project is sufficiently distinct from the other projects in this course and is not based on the old CS50W Pizza project.

It is neither a social network project nor an e-commerce project. It utilizes Django (with 3 models) and JavaScript.

It is more complex than the other projects as it also uses Django Channels, Redis and Custom Authentication.

The web application is mobile-responsive with the help of Bootstrap and some custom CSS media queries.

## Files Overview

|         Filename/Directory          |     Description       |
|   :---:   |   :---: |
| ``capstone/asgi.py``     | Contains configuration for running http and websockets using ASGI. |
| ``capstone/settings.py`` | Standard django settings file with additional settings for authentication and channels. |
| ``capstone/urls.py``     | Contains the project url patterns. The url patterns for users and consultation apps. |
| ``consultation/consumers.py`` | Contains the Async chat consumer for the consultation. Handles the websocket events. |
| ``consultation/models.py``    | Contains the model structure for consultation and messages. |
| ``consultation/routing.py`` | Contains the websocket url routing for the consultation app. |
| ``consultation/static/consultation/`` | Contains the JavaScript file for the consultation template. |
| ``consultation/templates/consultation/`` | Contains the 3 templates for the consultation app. |
| ``consultation/urls.py``     | Contains the urls for starting, viewing consultations and chat. |
| ``consultation/views.py``     | Contains the view functions for starting, viewing consultations and chat. |
| ``users/forms.py``     | Contains the registration forms for consultants and patients. |
| ``users/models.py``     | Contains the custom user model extending the AbstractUser. |
| ``users/static/users/`` | Contains the `styles.css` file for styling the templates. |
| ``users/templates/users/`` | Contains 4 templates including a `layout.html` template. |
| ``users/urls.py``     | Contains the urls for homepage, register, login and logout. |
| ``users/views.py``     | Contains the views for homepage, register, login and logout. |



## How to run

### To run this project locally, follow these steps

1. Clone this repo or download zip

2. Unzip it

3. In a terminal, navigate to the project directory

4. Create virtual environment, [Link for more details](https://packaging.python.org/en/latest/guides/installing-using-pip-and-virtual-environments/#creating-a-virtual-environment)
```
python -m venv env or python3 -m venv env
```

5. Activate the virtual environment
```
env\Scripts\activate or source env/bin/activate
```

6. Install the requirements
```
pip install -r requirements.txt or pip3 install -r requirements.txt
```

7. Install [Docker](https://www.docker.com/get-docker) or [Redis](https://redis.io/download/) to run redis
```
docker run -p 6379:6379 -d redis:5 or redis-server
```

8. Run the django server
```
python manage.py runserver or python3 manage.py runserver
```

9. Go to the specified url and Enjoy!

## Acknowledgements and References

Referenced the previous projects and distribution code written by the staff for us.

[Django Documentation](https://docs.djangoproject.com/en/)

[Django Channels Documentation](https://channels.readthedocs.io/en/stable/)

Tutorials Referred:

[Channels Documentation Tutorial](https://channels.readthedocs.io/en/stable/tutorial/index.html)

https://youtu.be/RVH05S1qab8

https://youtube.com/playlist?list=PLPSM8rIid1a2UQnLjcAo9vTTtZH2aLpjO

[Bootstrap Docs](https://getbootstrap.com/docs/5.1/getting-started/introduction/)

[Bootstrap Icons](https://icons.getbootstrap.com/)