## DATABASE CREATION
# Steps
1. Import module path in order to get the path of certain file:
from os import path

2. Create a function for creating a database
def create_database(app):
    if not path.exists('website/' + DB_NAME):
        db.create_all(app=app)
        print('Created Database!')
2.1 Make a condiction (if) inside the function to check that the database doesn't exist
    if not path.exists('website/' + DB_NAME):

2.3 Create databe and print a message:
db.create_all(app=app)
        print('Created Database!')

All together looks like this:
def create_database(app):
    if not path.exists('website/' + DB_NAME):
        db.create_all(app=app)
        print('Created Database!')


3. Inside function <create_app>, import the class Note and User:
 from .models import User, Note

4. Inside function <create_app>, call the function <create_database>
    create_database(app)