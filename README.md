# Digital-Wallet-System

print("💳 Welcome to Digital Wallet")

# Initial balance
balance = 0.0

while True:
    print("\n----- MENU -----")
    print("1. Add Money")
    print("2. Send Money")
    print("3. Check Balance")
    print("4. Exit")

    choice = input("Enter your choice: ")

    # Add Money
    if choice == "1":
        amount = float(input("Enter amount to add: "))
        
        if amount > 0:
            balance = balance + amount
            print("Money added successfully!")
        else:
            print("Invalid amount!")

    # Send Money
    elif choice == "2":
        amount = float(input("Enter amount to send: "))
        
        if amount <= balance and amount > 0:
            balance = balance - amount
            print("Money sent successfully!")
        else:
            print("Insufficient balance or invalid amount!")

    # Check Balance
    elif choice == "3":
        print("Your current balance is: ₹", balance)

    # Exit
    elif choice == "4":
        print("Thank you for using Digital Wallet!")
        break
