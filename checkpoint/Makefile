## Makefile includes instructions on environment setup 
# and lint tests.
# 1. Venv is created and activated.
# 2. Dependencies are installed using requirements.txt.
# 3. Dockerfile passes hadolint
# 4. app.py passes pylint
# (Optional) Build a simple integration test

setup:
	# Create python virtualenv & source it
	# source ~/.devops/bin/activate
	# python -m env ~/.capstone

install:
	# This should be run from inside a virtualenv
	# pip install --upgrade pip && pip install -r requirements.txt

lint:
	# See local hadolint install instructions:   https://github.com/hadolint/hadolint
	# This is linter for Dockerfiles
	hadolint Dockerfile
	# This is a linter for Python source code linter: https://www.pylint.org/
	# This should be run from inside a virtualenv
	pylint --disable=R,C,W1203 app.py

all: install lint test
