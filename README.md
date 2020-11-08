# flask-microservice-users-with-jwt-extended

## Requirements

Config virtualenv:

```bash
git clone https://github.com/eadomenech/flask-microservice-users-with-jwt-extended.git src
python3 -m venv env
source env/bin/activate
pip install -r src/requirements.txt
```

## For development

```bash
pip install pytest==5.0.1 pytest-cov flake8
```

Create local postgres database and configure:

```bash
export FLASK_APP=app.py
export DATABASE_DEV_URL=postgres://user:password@host:5432/database-name
flask db init
flask db migrate
flask db upgrade
```

Run tests:

```bash
pytest --cov-report term-missing --cov
```

Code quality:

```bash
flake8 application tests
```

## Run the app

```bash
python app.py
```
