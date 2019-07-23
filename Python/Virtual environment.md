# Python Virtual Environment
---------------


- create virtualenv with specific python version
```python
virtualenv -p /usr/bin/python3.7 env-name
# using venv
python3 -m venv env-name
```
- `deactivate` - return to global environment
- `source myenv/bin/activate` - activates environment

- download all modules into text file
```python
pip freeze --local > requirements.txt
```

- project packages with pipreqs
```python
pip install pipreqs
pipreqs project_folder
```

- install from requirements file
```python
pip install -r requirements.txt
```

# Virtual env in Windows10 using VENV

create new virtual env

```python
python -m venv project_name`
```
activate virtual env

```python
source project_name/Scripts/activate
```
---
### References

[Pipenv & Virtual Environments](https://docs.python-guide.org/dev/virtualenvs/)
