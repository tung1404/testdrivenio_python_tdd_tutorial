# Blog App

Tutorial based on: https://testdriven.io/blog/modern-tdd/

--- 

## Prepare the environment

- Create and activate the virtual environment
```
python3 -m venv venv
source venv/bin/activate
```

- Install the requirements
```
pip install -r requirements.txt
```


## Run tests

- Run the unit/integration tests
```
python -m pytest -v tests
```

- Run the test coverage
``` 
python -m pytest tests --cov=blog 
```

- Run the E2E tests
```
export PYTHONPATH=$PYTHONPATH:$PWD
export FLASK_APP=blog/app.py 

python -m flask run
python -m pytest tests -m 'e2e'
```
