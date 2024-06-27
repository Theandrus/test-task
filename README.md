**Getting Started with Building The App**

Run command: `sudo docker-compose up --build` 

Then you can go to DefaultRouter of the REST Api
Use _0.0.0.0:1515_ or _localhost:1515_ with these API's:
* **CREATE**: Use POST to _/teams/_ or _/people/_ to create new entries.
* **READ**: GET from _/teams/_ or _/people/_ for lists, or _/teams/{id}/_ or _/people/{id}/_ for specific entries.
* **UPDATE**: Use PUT or PATCH on _/teams/{id}/_ or _/people/{id}/_ to update entries.
* **DELETE**: DELETE at _/teams/{id}/_ or _/people/{id}/_ to remove entries.

Also you can use Django admin-panel for adding new models(teams and people)
You have to enter 'web' container. Run command(when docker containers is running): `sudo docker-compose exec web bash`
after that run commands(only in this order): 
    `python manage.py makemigrations` -> `python manage.py migrate` -> `python manage.py create superuser`
It will create a superuser, and now you can enter to admin-panel with your username and password,
use: _localhost:1515/admin/_ or _0.0.0.0:1515/admin/_