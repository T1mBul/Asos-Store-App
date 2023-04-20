# Store Asos Server

**_This project was made for educational purposes._**

_In it, I learned how to work with such services as: Redis, Celery, Nginx, Gunicorn (when deploying a project to production). 
PostgreSQL database: pgAdmin, database deployment on the prod, dump and upload data. 
Django tools were studied: Django-Debug-Toolbar, Django unittest, Django-extenstions (shell_plus),
Django admin (adding fields in the admin panel, working with these fields), Django-environ for settings project.
An email confirmation system was implemented through background tasks (redis, celery).
Work was carried out with the Stripe payment system: obtaining an Api key and a Webhook key to pull up data from the payment system. 
Two options for storing information about goods were tested - on the side of the payment service and in our database. 
The project is an online store with goods. Each user can register using GitHub and log in to his account, where the ability to edit data in fields has been added.
Also, each user can register using the usual registration form.
After authentication, the user can add products to the cart, there will be a list of products and their cost, and the total amount of the basket at the bottom. 
After that, by clicking on the pay button, the user will go to the payment page (stripe), in which the data of the payment instrument is filled in. 
Then the user will be redirected to the appropriate page (successful payment/refused). 
The user has a page for viewing his orders, in which the following fields are: order date, status, cost and the button "more about the order". 
If you go to the details page, then there is all the information about the order made: the list of products, their cost, the total cost._

#### Stack:

- [Python](https://www.python.org/downloads/)
- [PostgreSQL](https://www.postgresql.org/)
- [Django](https://www.djangoproject.com/)
- [Stripe](https://stripe.com/)
- [Redis](https://redis.io/)
- [Celery](https://docs.celeryq.dev/en/stable/index.html)

## Local Developing

All actions should be executed from the source directory of the project and only after installing all requirements.

1. Firstly, create and activate a new virtual environment:
   ```bash
   python -m venv ../venv
   source ../venv/Scripts/activate
   ```
   
2. Install packages:
   ```bash
   pip install --upgrade pip
   pip install -r requirements.txt
   ```
   
3. Run project dependencies, migrations, fill the database with the fixture data etc.:
   ```bash
   ./manage.py migrate
   ./manage.py loaddata <path_to_fixture_files>
   ./manage.py runserver 
   ```
