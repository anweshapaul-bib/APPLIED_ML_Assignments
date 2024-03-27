# Containerization & Continuous Integration 

This assignment is an implementation of a Flask web application for classifying text as spam or not spam using a trained Support Vector Machine (SVM) model. The application provides an API endpoint `/classify` that accepts a JSON request with a `sentence` key, and returns a JSON response indicating whether the sentence is classified as spam or not, along with the propensity score.

## Prerequisites

- Python 3.7 or higher
- pip (Python package installer)

## Installation

1. Clone the repository:

```bash
git clone https://github.com/your-username/spam-classification-flask.git
```

2. Navigate to the project directory:

```bash
cd spam-classification-flask
```

3. Create a virtual environment (optional but recommended):

```bash
python -m venv env
source env/bin/activate  # On Windows, use `env\Scripts\activate`
```

4. Install the required packages:

```bash
pip install -r requirements.txt
```

## Running the Application

1. Start the Flask application:

```bash
python app.py
```

The application will run on `http://localhost:5000` by default.

2. To classify a sentence, send a POST request to `http://localhost:5000/classify` with a JSON payload containing the `sentence` key:

```bash
curl -X POST -H "Content-Type: application/json" -d '{"sentence": "Your sentence here"}' http://localhost:5000/classify
```

The response will be a JSON object with a `result` key containing the classification result and propensity score.

## Testing

The project includes unit tests for the scoring function and Flask application. To run the tests, execute the following command:

```bash
python test.py
```

## Docker Container

The project includes a Dockerfile for building a Docker container. To build and run the container, follow these steps:

1. Build the Docker image:

```bash
docker build -t spam-classification-flask .
```

2. Run the Docker container:

```bash
docker run -p 5000:5000 spam-classification-flask
```
