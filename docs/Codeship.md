# Codeship
Codeship is a Continuous Delivery system.  See https://codeship.com for more
information.

Below test script configurations so the testing will use PostgreSQL on 
Codeship.

#Setup Commands
```
# Setup PostgreSQL 9.3
#https://codeship.com/documentation/databases/postgresql/
psql -c 'create database $PG_USER;'
psql -c 'alter database $PG_USER owner to $PG_USER;'
psql -c 'alter user $PGUSER createdb;'
DATABASE_URL='postgres://$PG_USER:$PG_PASSWORD@127.0.0.1:5432/$PG_USER'

pip install -r requirements.txt

# Sync your DB for django projects
# python manage.py syncdb --noinput

# Run migrations for your django project
# python manage.py migrate --noinput
```

#Test Commands
```
# Running your Django tests
python manage.py test

# You can also run your own python scripts
# python run_tests.py
# Or use fabric to run your tests
# fab test
```
