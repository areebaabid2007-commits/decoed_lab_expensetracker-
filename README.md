# decoed_lab_expensetracker-
A user-friendly Expense Tracker that helps users record, categorize, and manage their expenses. It provides a clear overview of spending, making it easier to monitor finances, stay organized, and manage budgets effectively.
💰 Expense Tracker

📌 About the Project

The Expense Tracker is a web application used to record and manage daily expenses. It helps users keep track of their spending and calculate their total expenses.

❓ Why Is It Used?

It is used to:

- Track daily expenses
- Manage personal finances
- Calculate total spending
- Understand spending habits
- Keep financial records organized

⚙️ How It Works

The user enters the expense name and amount. When the Add Expense button is clicked, JavaScript creates a new expense and displays it in the expense list. The total amount is then updated automatically.

💻 Main Code

HTML

<input type="text" id="expenseName" placeholder="Expense name">
<input type="number" id="expenseAmount" placeholder="Amount">
<button onclick="addExpense()">Add Expense</button>

<ul id="expenseList"></ul>
<h3>Total: $<span id="total">0</span></h3>

JavaScript

let total = 0;

function addExpense() {
    let name = document.getElementById("expenseName").value;
    let amount = Number(document.getElementById("expenseAmount").value);

    if (name === "" || amount <= 0) {
        alert("Please enter valid details");
        return;
    }

    let listItem = document.createElement("li");
    listItem.textContent = `${name}: $${amount}`;

    document.getElementById("expenseList").appendChild(listItem);

    total += amount;
    document.getElementById("total").textContent = total;

    document.getElementById("expenseName").value = "";
    document.getElementById("expenseAmount").value = "";
}

🛠️ Technologies Used

- HTML – Creates the structure.
- CSS – Styles the application.
- JavaScript – Adds expenses, calculates the total, and updates the webpage dynamically.

🎯 Purpose

This project was created as part of my Decode Labs project to practice HTML, CSS, JavaScript, DOM manipulation, and building a practical finance management application.