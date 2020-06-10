# azure-ml-devops
Azure DevOps workflow for ML

## Steps to run this project

* Create a Github Repo (if not created)
* Open Azure Cloud Shell
* Create ssh-keys in Azure Cloud Shell
* Upload ssh-keys to Github
* Create scaffolding for project (if not created)
  - Makefile

Should look similar to the file below

```bash
install:
	pip install --upgrade pip &&\
		pip install -r requirements.txt

test:
	python -m pytest -vv test_hello.py


lint:
	pylint --disable=R,C hello.py

all: install lint test
```

  - requirements.txt
* The requirements.txt should include:

```bash
pylint
pytest
```
* Create a python virtual environment and source it if not created

```bash
python3 -m ~/.myrepo
source ~/.myrepo/bin/activate
```

* Run `make all` which will install





