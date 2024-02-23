# Creating a virtual environment in linux terminal

```python
python3 -m venv .venv
```

# Activating the virtual environnement

```python
source .venv/bin/activate
```

# Defining environment variables for the Flask application  

```python
export set FLASK_APP=application.py
```

```python
export set FLASK_ENV=development
```

# Run application

```python
flask run
```

# To create the Database of our Flask application

1. Open an python terminal

```python
python3.10
```

2. Create the database

```python
from application import app, db
app.app_context().push()
db.create_all()
```

3. Create the object to add in our Database

drink = Drink(name="Grape Soda", description="Tastes like grapes")

4. Check if the object has been actually created

```python
drink
```

5. Add the object in our DB

```python
db.session.add(drink)
db.session.commit()
```

6. Query the DB to show all objects

```python
Drink.query.all()
```

7. Add objects

```python
db.session.add(Drink(name="Cherry", description="Tastes like that one ice cream"))
db.session.commit()
```

8. Ext the Python terminal

```python
exit()
```

9. Go back and run the application

```python
flask run
```