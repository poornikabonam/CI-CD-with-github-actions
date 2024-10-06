# Simple Flask App with CI/CD Pipeline

This is a simple Flask web application that returns "Hello, World!" when accessed. The project includes a CI/CD pipeline using GitHub Actions and Docker to automate the build, test, and deployment process.

## Project Structure

- **`app.py`**: The main Flask application that defines a single route.
- **`requirements.txt`**: Lists the dependencies for the project (Flask and pytest).
- **`Dockerfile`**: Docker configuration to containerize the Flask app.
- **`.github/workflows/ci-cd.yaml`**: GitHub Actions pipeline for CI/CD.

## Prerequisites

To run this project locally, ensure you have the following installed:
- Python 3.7 or higher
- Docker
- Git

## Getting Started

```bash
# 1. Clone the repository
git clone https://github.com/yourusername/simple-flask-app.git
cd simple-flask-app

# 2. Install the dependencies
pip install -r requirements.txt

# 3. Run the Flask app locally
python app.py
# The app will be available at http://localhost:5000

# 4. Run the tests using pytest
python -m pytest

# 5. Build the Docker image
docker build -t simple-flask-app .

# 6. Run the Docker container
docker run -p 5000:5000 simple-flask-app
