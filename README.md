# calculator-frontend
Frontend for separated calculator system

```
# calculator-frontend
## Project Introduction
Frontend page for separated web calculator. It provides clickable calculator buttons, sends calculation requests to backend API, displays calculation results and historical records, and supports clearing history.

## Tech Stack
HTML, CSS, JavaScript (pure native, no framework)

## Operating Environment
Any modern web browser (Chrome, Edge, Firefox)

## Installation
1. Clone this repository
```bash
git clone https://github.com/YourUserName/calculator-frontend.git
cd calculator-frontend
```

2. No dependency installation required.

## Start Method

Open `index.html` directly in browser.

## Configuration

Modify the backend API address inside index.html to match your backend server IP and port.
Example: `const baseUrl = "shturl.cc/Y515p7IoXxhEvhi8B"`

## Connect with Backend

The frontend sends HTTP POST requests to backend API endpoint `/calculate` for computation, and GET request to `/history` to fetch records. Ensure backend service is running and port 5000 is open.

## Other Notes

Frontend only handles UI interaction. All mathematical calculation logic is executed on backend.

```

# 2、后端仓库 README.md（calculator-backend）
```markdown
# calculator-backend
## Project Introduction
Flask backend service for web calculator. All arithmetic operations run on server. It supports expression calculation, error handling (division by zero, invalid expression), and persists calculation history with SQLite.

## Tech Stack
Python 3, Flask, SQLite3

## Operating Environment
Python 3.8 or higher, Windows / Linux

## Installation
1. Clone repository
```bash
git clone https://github.com/YourUserName/calculator-backend.git
cd calculator-backend
```

2. Install dependencies

```
pip install flask
```

## Start Method

```
python app.py
```

Service listens on `0.0.0.0:5000`

## Configuration

Default port:5000. Modify port in app.py if needed.
Open firewall/security group 5000 TCP port for external access.

## Database Initialization

SQLite database `calculator.db` will be automatically created when the service first starts. No manual SQL script needed.

## Connect with Frontend

Backend provides REST API:

- POST `/calculate`: receive expression, return result
- GET `/history`: get calculation history
- DELETE `/history`: clear all history
Frontend needs to set its API address to this backend service address.

## Other Notes

- Keep the cmd/terminal window open while service running.
- Deploy on Tencent Cloud Light Application Server for public network access.
