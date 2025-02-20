# Dockerfile Bug: Unittest Discovery Failure

This repository demonstrates a common error in Dockerfiles: forgetting to install project dependencies before running tests.  The provided `Dockerfile` attempts to run unit tests using `unittest discover`, but it fails because the required packages are not installed.

The solution involves adding a `pip install -r requirements.txt` command to install the dependencies specified in a `requirements.txt` file.

## Bug Report

The original `Dockerfile` is missing the crucial step of installing project dependencies. This leads to a `ModuleNotFoundError` during the execution of unit tests.  This is a common mistake when building Docker images for projects with external dependencies.