
Flask Docker CI Demo 🚀

This is a simple DevOps project that demonstrates how to:
- Build a minimal Flask web application
- Write unit tests using Python's built-in `unittest`
- Containerize the app using Docker
- Automate testing with GitHub Actions CI

📁 Project Structure
---------------------
flask-docker-ci/
├── app/
│   ├── __init__.py
│   └── main.py
├── tests/
│   ├── __init__.py
│   └── test_app.py
├── Dockerfile
├── requirements.txt
├── .github/workflows/ci.yml
└── README.txt

🧰 Tech Stack
-------------
- Python 3.10
- Flask 2.2.5
- Docker
- GitHub Actions
- unittest

🚀 Running the App Locally
---------------------------
1. Clone the Repo:
   git clone https://github.com/kornerstonecoker/flask-docker-ci.git
   cd flask-docker-ci

2. Create & Activate a Virtual Environment:
   python3 -m venv .venv
   source .venv/bin/activate

3. Install Dependencies:
   pip install -r requirements.txt

4. Run the App:
   python app/main.py

   Visit: http://localhost:5000

🧪 Run Tests
-------------
   python -m unittest discover tests

🐳 Docker Usage
----------------
Build the Docker Image:
   docker build -t flask-ci .

Run the Container:
   docker run -d -p 5000:5000 flask-ci

⚙️ CI/CD with GitHub Actions
-----------------------------
This project uses GitHub Actions to automatically:
- Set up Python 3.10
- Install dependencies
- Run unit tests on every push to `main`

🛠️ CI Pipeline Issues & Fixes
-------------------------------

❌ Issue 1: Python 3.1 Not Found
Error:
   The version '3.1' with architecture 'x64' was not found for Ubuntu 22.04.
Fix:
   Corrected python-version in ci.yml to '3.10'

❌ Issue 2: Deprecated werkzeug.__version__
Fix:
   Updated version detection to use:
   from importlib.metadata import version
   print(version("werkzeug"))

❌ Issue 3: Dependency Conflict
Error:
   Flask 2.2.5 requires werkzeug >=2.2.0, but we initially pinned <2.1.0.
Fix:
   Updated requirements.txt to:
   Flask==2.2.5
   werkzeug>=2.2.0,<3.0.0

📜 License
-----------
MIT License

🙌 Author
----------
Built by @kornerstonecoker – feel free to connect!
