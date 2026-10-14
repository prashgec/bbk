# Week 1 University API

A small FastAPI application that exposes sample university student data.

## Setup

From the repository root, enter the project directory and install its dependencies:

```sh
cd week1-university-api
python -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
```

## Run

```sh
uvicorn main:app --reload
```

The API runs at `http://127.0.0.1:8000`. Interactive documentation is available at `/docs`.

## Endpoints

| Method | Path | Description |
| --- | --- | --- |
| `GET` | `/` | API name, version, and endpoint summary |
| `GET` | `/students/` | All students, keyed by student ID |
| `GET` | `/students/{student_id}` | A student record; returns `404` when the ID is unknown |

Example:

```sh
curl http://127.0.0.1:8000/students/s1
```

## Tests

Run the tests from this directory with Python's built-in test runner:

```sh
python -m unittest discover -s tests -v
```