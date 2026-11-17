# Student API

A RESTful API built with **FastAPI** and served via **Uvicorn**.

---

## Project Structure

```text
student-api/
│
├── .venv/               # Local virtual environment (created during setup, ignored by Git)
│
├── app/
│   ├── __init__.py      # Marks 'app' as a Python package
│   └── main.py          # FastAPI application entry point
│
├── .gitignore           # Specifies files/folders excluded from Git
└── requirements.txt     # Locked project dependencies
```

---

## Setting Up on a New Machine

Follow these steps to set up and run the project locally after cloning the repository.

### 1. Clone the Repository
```bash
git clone <https://github.com/auxalus/oculus-monorepo.git>
cd student-api
```

### 2. Verify Python Installation
Ensure Python 3 (version 3.8 or higher recommended) is installed on your machine:
```bash
python3 --version
```

### 3. Create a Virtual Environment
Create an isolated virtual environment inside the project root directory:
```bash
python3 -m venv .venv
```

### 4. Activate the Virtual Environment
Activate the environment before installing dependencies or running the server:

* **macOS / Linux:**
  ```bash
  source .venv/bin/activate
  ```
* **Windows (Command Prompt / PowerShell):**
  ```cmd
  .venv\Scripts\activate
  ```


### 5. Install Dependencies
Install all required packages from `requirements.txt`:
```bash
pip install -r requirements.txt
```

---

## Running the Application

Start the local development server with auto-reload enabled:
```bash
uvicorn app.main:app --reload
```

Once the server is running, access the API and its auto-generated documentation in your browser:
* **API Root:** `http://127.0.0.1:8000`
* **studdent** `http://127.0.0.1:8000/student`
* **health:** `http://127.0.0.1:8000/health`

---

## Managing Dependencies (For Contributors)

If you install any new packages while developing, update `requirements.txt` before committing your changes so other machines stay in sync:
```bash
pip freeze > requirements.txt
```