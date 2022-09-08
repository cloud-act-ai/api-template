# Hello

This is a repo for app Hello; bootstrapped by DevStream.

By default, the automatically generated scaffolding contains:

- a piece of sample Python [Flask](https://flask.palletsprojects.com/en/2.2.0/) web app
- sample unittest
- .gitignore
- requirements.txt
- wsgi.py
- Dockerfile
- Helm chart

## Dev

### Run Locally

```shell
python3 -m venv .venv
. .venv/bin/activate
pip install -r requirements.txt
flask --app app/hello.py run
```

### Run in Docker

```shell
docker build . -t hello:latest
docker run -it -d -p 8080:80 hello:latest
```

### Run in K8s

```shell
# install
helm install hello helm/hello/

# uninstall
helm delete hello
```

## Test

```shell
python3 -m unittest
```
