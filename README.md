# Subscription Management System(SubManager)

## Project overview
SubManager is a web base software application designed to help subscribers track, upgrade, and cancel their recurring subscription plans, providing system administrators with centralized pricing tier management.

## Software architecture
This application is designed to follow a 3-Tier Layered Architecture:
- **Presentation Layer(Frontend):** Web base user interface for subscriber interactions and input forms.
- **Business Logic Layer(Backend):** Node.js and API server handling user authentication, payment validation, and subscription status state changes.
- **Data Layer(Database):** MongoDB Atlas database storing for persistent user accounts, subscription records, and price tiers.

## Prerequisites & Dependencies
- Node.js(v22 or higher)
- Git version control
- MongoDB Atlas account

## Local setup and running instructions
1. Clone the repository to your local device:
   `git clone https://github.com/JoonhoKwon/[your repository name here].git`
2. Install dependencies for both frontend and backend:
   `npm run install-all`
3. Configure environmental secrets in the `.env` file inside the backend directory:
   - `MONGO_URI`
   - `JWT_SECRET`
   - `PORT`
4. Start the application:
   `npm start`

## Public deployment URL
- **AWS EC2 Deployment URL:** `http://<EC2-PUBLIC-IP>`

## Project limitation
- Payment process only accept card format payment rather than live banking payment.
- Multi-currency system should be supported.