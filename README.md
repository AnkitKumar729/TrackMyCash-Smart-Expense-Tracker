# TrackMyCash-A Smart Expense Tracker
TrackMyCash

TrackMyCash is a React-based personal finance management application designed to help users track their income, expenses, and overall financial health. It integrates with the Plaid API to fetch financial data (e.g., card transactions) and uses MongoDB for data storage. The app features an intuitive interface with transaction management, financial overviews, and data visualizations through charts, along with user authentication and profile management.

Screenshots

Main Dashboard
![image alt](https://github.com/AnkitKumar729/TrackMyCash-Smart-Expense-Tracker/blob/68f0ba9f2fe10a48af5f8e60c1a830f29314ed6b/Dashboard.png)

View your financial overview, recent transactions, and income/expense trends.
![image alt](https://github.com/AnkitKumar729/TrackMyCash-Smart-Expense-Tracker/blob/68f0ba9f2fe10a48af5f8e60c1a830f29314ed6b/Income.png)

Real-time Sync with Cards
![image alt](https://github.com/AnkitKumar729/TrackMyCash-Smart-Expense-Tracker/blob/68f0ba9f2fe10a48af5f8e60c1a830f29314ed6b/Cards.png)

Charts

![image alt](https://github.com/AnkitKumar729/TrackMyCash-Smart-Expense-Tracker/blob/68f0ba9f2fe10a48af5f8e60c1a830f29314ed6b/Cards.png)


Table of Contents

Features
Prerequisites



Installation



Environment Variables



Usage







Technologies Used



Contributing



License

Features





Dashboard Layout: Responsive layout with a sidebar (SideMenu.jsx) and navbar (Navbar.jsx) for navigation.



Financial Overview: Visualize total balance, income, and expenses with a pie chart (FinanceOverview.jsx).



Income Tracking:





Add income via a form (AddIncomeForm.jsx) with source, amount, date, and icon selection (EmojiPickerPopup.jsx).



View recent income (RecentIncome.jsx) and detailed lists (IncomeList.jsx) with CSV and PDF export.



Bar chart for income trends (IncomeOverview.jsx).



Expense Tracking:





Add expenses via a form (AddExpenseForm.jsx) with category, amount, date, and icon selection.



View recent expenses (ExpenseTransaction.jsx) and detailed lists (ExpenseList.jsx) with CSV and PDF export.



Line chart (ExpenseOverview.jsx) and bar chart (Last30DaysExpenses.jsx) for expense trends.



Transaction Management: Display transactions with icons, dates, and amounts (TransactionInfoCard.jsx) with month-based filtering (RecentTransactions.jsx).



Plaid API Integration: Fetch financial data (e.g., card transactions) using Plaid API credentials.



User Profile: Display user avatar (CharAvatar.jsx) or profile photo (ProfilePhotoSelector.jsx) with upload/remove functionality.



Authentication: Clean authentication page (AuthLayout.jsx) with a stats card, backed by MongoDB and JWT.



Modal and Alerts: Reusable modal (Model.jsx) and delete confirmation alert (DeleteAlert.jsx).



Custom Charts: Bar (CustomBarChart), pie (CustomPieChart), and line (CustomLineChart) charts for data visualization.



Responsive Design: Mobile-friendly with a toggleable sidebar.

Prerequisites





Node.js: Version 14.x or higher.



MongoDB: A running MongoDB instance (local or cloud, e.g., MongoDB Atlas).



Plaid Account: Sign up at Plaid to obtain PLAID_CLIENT_ID, PLAID_SECRET, and set PLAID_ENV (e.g., sandbox for testing).



Git: For version control.

Installation





Clone the Repository:

git clone https://github.com/your-username/trackmycash.git
cd trackmycash



Install Dependencies:

npm install

This installs dependencies like react, react-icons, moment, jspdf, papaparse, emoji-picker-react, and others.



Set Up Environment Variables:





Copy .env.example to .env:

cp .env.example .env



Edit .env to add your own credentials (see Environment Variables).



Start the Backend Server:





Ensure your MongoDB instance is running.



Start the backend (assuming a Node.js/Express backend):

npm run server



The server runs on PORT (default: 8000).



Start the Frontend Development Server:

npm start

The app will be available at http://localhost:3000.

Environment Variables

Create a .env file in the project root and configure the following variables. Do not use the example credentials provided in the repository's documentation, as they are sensitive. Obtain your own credentials for MongoDB and Plaid.

MONGODB_URI=your_mongodb_uri_here
JWT_SECRET=your_jwt_secret_here
PORT=8000
PLAID_CLIENT_ID=your_plaid_client_id_here
PLAID_SECRET=your_plaid_secret_here
PLAID_ENV=sandbox
