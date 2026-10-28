# Learning Docker

A minimal Flask app packaged as a Docker image.

## Why this exists
A first exercise in containerising a Python app, as groundwork for MLOps deployments.

## What it does
- Serves a form at `/` that asks for your name
- Returns a greeting at `/greet`
- Builds into a `python:3.8-slim` image that runs on port 5000

## Project structure
```
docker_mlops_learning/
├── app.py            Flask app
├── dockerfile        Container image definition
├── requirements.txt  Python dependencies
└── LICENSE           MIT licence
```

## Getting started
Requirements: Docker (or Python 3.8+ to run without it).
```bash
git clone https://github.com/abhijha8287/docker_mlops_learning.git
cd docker_mlops_learning
docker build -t flask-greet -f dockerfile .
docker run -p 5000:5000 flask-greet
```
Open http://localhost:5000.

Without Docker:
```bash
pip install -r requirements.txt
python app.py
```

## Tech stack
Python, Flask, Docker

## Notes
MIT licensed.
