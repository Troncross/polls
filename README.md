# mysite
This is a version of the official Django tutorial application configured for deployment into a production environment on Heroku.

Done with part 6 of the official Django tutorial.
 https://docs.djangoproject.com/en/1.7/intro/tutorial06

# Getting started
Start your DAD virtual environment.
```
& $Env:WORKON_HOME\DAD\Scripts\activate.ps1
```
Change to your project directory
```
cd $Env:PROJECT_HOME\DAD
```
Then clone this repository.  
```
git clone git@github.com:usma-it394/mysite.git
```

Change your current working directory to the clone'd project directory.
```
cd mysite
```
Install the packages from requirements.txt (you probably already have these installed in your DAD environment):
```
pip install -r requirements.txt
```

Then set the DATABASE_URL environment variable. Finally, create the initial database structure and interactively create the initial security principal with:
```
python manage.py syncdb
```

You can view the polls app running locally by starting the project with
```
python manage.py runserver
```
# Deployment
The in-class exercise from lesson 04 covers steps how to deploy into the production environment on Heroku.

# Misc

You can see the deployed version at http://usma-it394-polls.herokuapp.com/polls/
