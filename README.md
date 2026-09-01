# Subscription Management System(SubManager)

## 1. Project overview
SubManager is a web base software application designed to help subscribers track, upgrade, and cancel their recurring subscription plans, providing system administrators with centralized price tier management.

## 2. Software architecture
This application is designed to follow a 3-tier layered architecture:
- **Presentation Layer(Frontend):** Web base user interface based on React.js for subscriber interactions and input forms.
- **Business Logic Layer(Backend):** Node.js and REST API server handling user authentication, input validation, and subscription status state changes.
- **Data Layer(Database):** MongoDB Atlas database storing for persistent user accounts, subscription records, and price tiers.

## 3. Prerequisites
If setting up this application, ensure the following software is installed prior to running the setup commands.
- **Git Version Control:** Download and install from [git-scm.com](https://git-scm.com/).
- **Node.js(v22 or higher)& npm:** Download and install from [nodejs.org](https://nodejs.org/).
- **Code Editor:** Visual Studio Code from [code.visualstudio.com](https://code.visualstudio.com/).
- **MongoDB Atlas Cloud Account:** Create a free MongoDB database from [mongodb.com](https://account.mongodb.com/).

## 4. Local setup and running instructions
**Clone the repository to your local device:**
Open your terminal (Mac/Linux) or Command Prompt/PowerShell (Windows) and clone the repository:
```bash
git clone https://github.com/JoonhoKwon/IFN636-A1.git
cd IFN636-A1
```

**Configure Environment Variables(.env)**
Navigate to the backend directory and create a new .env file.
Or you can create a file named .env inside backend/ and copy the contents from .env.example.
```bash
cd backend
cp .env.example .env
```
Paste the following environment variables inside backend/.env:
```bash
MONGO_URI=mongodb+srv://<your_username>:<your_password>@cluster0.xxx.mongodb.net/<your_database_name>?retryWrites=true&w=majority
JWT_SECRET=<your_secretkey_here>
PORT=5001
```
NOTE: Replace <your_username> and <your_password> with your actual MongoDB Atlas database credentials.
SECURITY NOTE: Never commit the .env file to Git. Please ensure the .env file is listed in .gitignore to prevent credential exposure.

**Install dependencies for both frontend and backend:**
```bash
cd ..
npm run install-all
```

**Start the application:**
```bash
`npm start`
```

## Known limitations
- Payment process only accept card format payment rather than live banking payment.
- Multi-currency system should be supported.

## Public deployment URL
- **AWS EC2 Deployment URL:** `http://54.153.191.190/`
- **Deployment Stack:** AWS EC2(Ubuntu) managed PM2 process manager and reverse-proxied through Nginx on HTTP Port 80.