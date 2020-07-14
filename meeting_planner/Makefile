TOP ?= .

venv:
	test -s venv || { virtualenv -p python $(TOP)/venv; }
	venv/bin/pip install -r $(TOP)/requirements.txt
