# endsem
class BankAccount:
    def __init__(self, account_number, balance=0):
        # Initialize the account with account number and an optional balance (defaults to 0)
        self.account_number = account_number
        self.balance = balance

    def deposit(self, amount):
        # Increase the balance by the deposited amount
        self.balance += amount
        print(f"Depositing {amount}")

    def withdraw(self, amount):
        # Check if balance is sufficient for withdrawal
        if amount > self.balance:
            print("Error: Insufficient funds for withdrawal.")
        else:
            self.balance -= amount
            print(f"Withdrawing {amount}")

    def get_balance(self):
        # Return and print the current balance
        print(f"Current balance: {self.balance}")
        return self.balance

# Create an instance of BankAccount with an account number "123456789"
account = BankAccount("123456789")

# Test deposit and withdrawal methods
account.deposit(5000)  # Deposit 5000
account.withdraw(2000)  # Withdraw 2000

# Print the final balance
account.get_balance()  # Get and print the current balance

