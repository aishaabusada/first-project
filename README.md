How to run
1-backend
Open your terminal inside the project directory and navigate to the backend folder (cd backend), then install the required dependencies using npm install express cors pg.

Create a PostgreSQL database named expense_tracker and execute the SQL statements from schema.sql to set up the expenses table.

Create a .env file in the backend directory and configure your database connection parameters (DB_USER, DB_PASSWORD, DB_HOST, DB_PORT, DB_NAME).

Start the backend server by running node server.js (or using nodemon server.js).

2-Frontend

Navigate to the frontend directory and open the index.html file directly in your browser (or use Live Server in VS Code).

Features
[x] Add an expense (with validation)

[x] Delete an expense

[ ] Edit an expense

[x] Filter by category

[x] Summary cards (total, count, highest)

[x] Data is saved in a PostgreSQL database

What was the hardest part?
The most challenging part of this project was setting up the asynchronous data flow between the PostgreSQL database, the Express REST API, and the dynamic frontend interface. Managing proper CORS configuration and ensuring that the summary cards dynamically recalculate totals and highest expenses immediately upon adding or deleting records required careful state management in vanilla JavaScript. I solved this by structuring clean API endpoints and chaining promise-based fetch functions to refresh the UI state seamlessly after every CRUD operation.