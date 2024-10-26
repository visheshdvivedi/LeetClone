# LeetCode Clone

A fully functional LeetCode-inspired platform for coding challenges, built with React and Django. This web application allows users to create accounts, solve programming problems, and track their progress through personal profiles.

## Features

- **User Authentication**: Secure login and registration system.
- **Dashboard**: View your progress, track solved problems, and monitor coding stats.
- **Coding Problems**: Explore a collection of coding challenges with a dedicated Problem Page for each.
- **Real-Time Code Execution**: Submit and run code in multiple languages using Judge0.
- **Responsive Design**: Accessible across all devices.
- **Interactive UI**: Dynamic landing page with hero section, features overview, and testimonials.

## Pages

- **HomePage**: Overview of the platform with sections on features, how it works, technologies, and developer info.
- **LoginPage & RegisterPage**: For user account creation and secure login.
- **DashboardPage**: Personalized user dashboard for managing progress.
- **ProblemPage**: Detailed coding challenge page with code editor and submission capabilities.

## Tech Stack
- **Frontend**: React, CSS
- **Backend**: Django, PostgreSQL
- **Code Execution**: Self-hosted Judge0


## Local Setup

### Prerequisites

- **NodeJS** (for frontend)
- **Python 3.8+** (for backend)
- **PostgreSQL** (for database)
- **Judge0** (for code execution)

### Steps

#### Step 1: Clone the repository
```cmd
git clone https://github.com/visheshdvivedi/LeetClone.git
cd leetclone
```

#### Step 2: Backend Setup (Django)

1. Navigate to the backend folder
```cmd
cd backend
```

2. Create and activate virtual environment
```cmd
python3 -m venv venv
source venv/bin/activate
```

3. Install the required dependencies
```cmd
pip3 install -r requirements.txt
```

4. Setup environment variables by creating a `.env` file and fill the following details:
```
BASE_API_URL=https://localhost:8000
BASE_APP_URL=https://localhost:5173/
DEBUG=True

GOOGLE_OAUTH_BACKEND_REDIRECT_URL=https://localhost:8000/api/v1/login/google/
GOOGLE_OAUTH_CLIENT_ID=<google auth client id>
GOOGLE_OAUTH_CLIENT_SECRET=<google auth client secret>
GOOGLE_OAUTH_FRONTEND_REDIRECT_URL=https://localhost:5173login/google

JUDGE_URL=<local judge0 instance url>

PGDATABASE=<database name>
PGHOST=<pg hostname>
PGUSER=<pg user>
PGPASSWORD=<pg password>
PGPORT=5432
```

5. Apply migrations 
```cmd
python3 manage.py makemigrations
python3 manage.py migrate
```

6. Create sample problems in database (optional)
```cmd
python3 manage.py createproblems problems_list.json
```

7. Run backend server
```cmd
python3 manage.py runserver
```

#### Step 3: Frontend

1. Navigate to the frontend folder

```cmd
cd frontend
```

2. Install the required dependencies
```cmd
npm install
```

3. Run the React development server
```cmd
npm run dev
```

#### Step 4: Setup Judge0 (Self Hosted)
- Follow the [Judge0 documentation ](https://github.com/judge0/judge0) to install and configure a self-hosted instance.
- Update the backend settings to point to your Judge0 instance for code execution.

#### Accessing the application
- Frontend: [http://localhost:5173](http://localhost:5173)
- Backend: [http://localhost:8000](http://localhost:8000)

Now you’re ready to start solving problems on your locally hosted LeetCode clone!

Build your coding skills and enhance your portfolio with a personalized coding platform. Get started with the repository and try solving problems just like on LeetCode!