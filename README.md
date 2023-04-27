# Python REST APIs With Flask, Connexion, and SQLAlchemy

- Python 3.8
- Flask 2.2.2

## Running the application

### Initialize the database (sqlite3)

```python
import sqlite3
conn = sqlite3.connect("people.db")
columns = [
    "id INTEGER PRIMARY KEY",
    "lname VARCHAR UNIQUE",
    "fname VARCHAR",
    "timestamp DATETIME",
]
create_table_cmd = f"CREATE TABLE person ({','.join(columns)})"
conn.execute(create_table_cmd)
```

To run the application locally, it's necessary to [pipenv](https://pipenv.pypa.io/en/latest/).

With `pipenv` installed, we can follow the steps below, through terminal.

```terminal
# start the development environment
$ pipenv shell

# install the dependencies
$ pipenv install --sync && pipenv install --dev

# run the application
$ python app.py
```

To populate the database, we can follow the steps below, through terminal.

```terminal
python build_database.py
```

## Documentation Routes

- `/api/ui/`: API documentation using Swagger.

---
