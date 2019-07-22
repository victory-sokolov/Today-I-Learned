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

# Virtual env in Windows10

In your Command Prompt navigate to your project:

`cd your_project`

Within your project:

`virtualenv env`

Activate your virtualenv: on Windows, virtualenv creates a batch file

`\env\Scripts\activate.bat`

to activate virtualenv on Windows, activate script is in the Scripts folder :

`\path\to\env\Scripts\activate`

---
### References

[Pipenv & Virtual Environments](https://docs.python-guide.org/dev/virtualenvs/)
