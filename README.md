# Flask-App-with-PostgreSQL-DB

This Website is build on the Python Flask with PostgreSQL Database. Data Insertion and Fetching.

**For Running on Local System Follow the below insturction**

Comment the below Code in the app.py File

'uri = os.getenv("DATABASE_URL")  # or other relevant config var
if uri.startswith("postgres://"):
    uri = uri.replace("postgres://", "postgresql://", 1)'
    
UnComment the Below code in the app.py file

app.config["SQLALCHEMY_DATABASE_URI"] = "sqlite:///User.sqlite3"
    
Run the app.py file and in the Terminal run the below commands

pyhton

from app import db

db.create_all()


**If you are Using libraries then run the pip freeze command and for the deployment on heroku follow the below commands**

UnComment the below Code in the app.py File

'uri = os.getenv("DATABASE_URL")  # or other relevant config var
if uri.startswith("postgres://"):
    uri = uri.replace("postgres://", "postgresql://", 1)'
    
Comment the Below code in the app.py file

app.config["SQLALCHEMY_DATABASE_URI"] = "sqlite:///User.sqlite3"


pip install gunicorn

pip install psycopg2

pip freeze > requirements.txt

Create runtime.txt and write your python version i.e python-3.7.10

echo web: gunicorn app:app > Procfile   #creating procfile

Create an account on heroku  and also download the heroku cli

##Write Following commands in pycharm/vscode
1. heroku login
2. heroku create "project name"
3. heroku addons:create heroku-postgresql:hobby-dev --app "project name"       
4. git init
5. git add . 
6. git commit -m "first commit"
7. heroku git:remote -a "project name"
8. git push heroku master
9. heroku run python
10. from app import db 
11. db.create_all()
