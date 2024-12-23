Name: Mayank raj
Company:CODTECH IT SOLUTION
ID:CT08DS388
Domain: Java programing
Duration:December 2024to January 2025
Mentor:Muzammil Ahmed

Overview of the Online Banking System Code
This Java program simulates a basic online banking system that supports common banking operations such as creating accounts, depositing and withdrawing funds, transferring money between accounts, viewing transaction history, and managing user information. It features a command-line interface for interacting with the system.

Key Components of the Program
1. Transaction Class:
Represents individual transactions like deposits, withdrawals, and transfers.
Stores transaction type (Deposit, Withdrawal, etc.), amount, transaction date, and balance after the transaction.
Provides a method getDetails() to format transaction details.
2. Account Class:
Represents a user's bank account with an account number and a balance.
Manages transactions using an ArrayList<Transaction>.
Provides methods for:
Deposit: Adds money to the account balance.
Withdraw: Deducts money from the account balance (if sufficient funds are available).
Transfer: Transfers money between accounts (either the same user’s accounts or between users).
View Transaction History: Displays a list of all transactions made on the account.
Includes a method getBalance() to retrieve the current balance of the account.
3. User Class:
Represents a user of the banking system with a username, password, email, and a list of accounts.
Manages user authentication through the authenticate() method.
Allows users to update their email address with the updateEmail() method.
Supports adding accounts to a user via the addAccount() method and retrieving an account by account number using getAccountByNumber().
4. BankSystem Class:
Acts as the core system to manage user interactions and operations.
Manages a collection of users (stored in a Map<String, User> where the key is the username).
Implements user login functionality with a simple authentication mechanism.
Provides a menu of options (e.g., deposit, withdraw, transfer, etc.) that users can choose from after logging in.
Includes methods to handle operations such as:
Create User: Registers a new user.
Login: Authenticates users by checking their username and password.
Create Account: Allows users to create a new bank account.
Deposit, Withdraw, Transfer, View Transaction History: Allows users to perform banking operations on their accounts.
Update Email: Allows users to change their registered email.
Runs a loop displaying the menu and processing user input until the user logs out.
5. Main Class:
The entry point of the application, where the program execution starts.
Instantiates the BankSystem object and runs it by calling the run() method.
How the Program Works:
User Creation & Login:

A new user is created by providing a username, password, and email. This user is stored in the system.
Existing users can log in using their username and password.
Account Management:

After logging in, the user can create new accounts with an initial balance.
Users can deposit money into their accounts, withdraw funds (if sufficient balance exists), and transfer funds between accounts.
Transaction History:

Every action (deposit, withdrawal, transfer) is logged as a transaction and can be viewed by the user via their account's transaction history.
Menu System:

A simple text-based menu allows users to select what operation they want to perform, such as creating an account, depositing or withdrawing money, transferring funds, viewing transaction history, or updating their email.
Basic Authentication:

The system checks the username and password provided by the user during login to authenticate the user before allowing them to access the banking system.
Loop & Interaction:

The system runs a loop where users are prompted with a menu after logging in. The program continues interacting with the user until they decide to log out.
