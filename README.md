Expense Management System 💰
A full-stack web application for tracking, categorising, and analysing personal expenses  built with FastAPI backend and Streamlit frontend, deployed on Streamlit Cloud.
🔗 Live Demo: https://expense-management-system-pf5bfxvkpbnwsjbj7mnjhh.streamlit.app
🎯 Project Overview
Built to demonstrate end-to-end full-stack development skills from REST API design and database modelling to interactive data visualisation and cloud deployment.
Key outcomes:

Automated 8-category expense classification
Real-time analytics dashboard surfacing spending patterns
REST API with full CRUD operations
Deployed and accessible via public URL

✨ Features

Add, update, and delete daily expenses by date
Categorise spending across 8 categories (Rent, Food, Shopping, Entertainment, and more)
Analytics dashboard with category breakdown and percentage distribution
Date range analysis for custom reporting periods
REST API backend for all expense operations
MySQL database for persistent storage

🛠️ Tech Stack
LayerTechnologyBackend APIFastAPI, UvicornFrontendStreamlitDatabaseMySQLData ProcessingPandasValidationPydanticTestingPytestDeploymentStreamlit Cloud



📁 Project Structure
Project-expense-tracking/
│
├── Backend/
│   ├── server.py          # FastAPI application
│   ├── db_helper.py       # Database operations
│   └── logging_setup.py   # Logging configuration
│
├── Fronted/
│   ├── app.py             # Main Streamlit application
│   ├── add_update_ui.py   # Add/Update expenses interface
│   └── analytics_ui.py    # Analytics dashboard
│
├── tests/
│   ├── backend/
│   │   └── test_db_helper.py
│   └── conftest.py
│
├── requirements.txt
└── README.md


🚀 Quick Start
1. Clone the repository
git clone <repository-url>
cd Project-expense-tracking
2. Create and activate virtual environment
python -m venv .venv
source .venv/bin/activate  # macOS/Linux
.venv\Scripts\activate     # Windows
3. Install dependencies
pip install -r requirements.txt
4. Configure database
Edit Backend/db_helper.py with your MySQL credentials:
connection = mysql.connector.connect(
    host="localhost",
    user="your_username",
    password="your_password",
    database="expense_management"
)

5. Run the application
Terminal 1 — Backend:
cd Backend
uvicorn server:app --reload --port 8000
Terminal 2 — Frontend:
cd Fronted
streamlit run app.py
Visit http://localhost:8501 in your browser.
🔌 API Endpoints
MethodEndpointDescriptionGET/expenses/{date}Get expenses for a datePOST/expenses/{date}Add or update expensesPOST/analytics/Get category breakdown

🧪 Testing
# Run all tests
pytest tests/

# Run with coverage
pytest --cov=Backend tests/
💡 What I Learned

Designing and deploying a production REST API with FastAPI
Connecting a live frontend to a backend API with error handling
Structuring a full-stack Python project for maintainability
Writing modular, testable code with Pytest
Deploying a data application to cloud infrastructure
