# cash-flow-manager-c
A simple Cash Flow Manager built in C to track income, expenses, and balance using structures and arrays.
# 💰 Cash Flow Manager (C Language)

A simple console-based Cash Flow Manager built using C.

## 📌 Features
- Add Income
- Add Expense
- View All Transactions
- View Current Balance
- Menu-driven program
- Uses Structures and Arrays

## 🛠 Technologies Used
- C Programming
- Structures
- Arrays
- Switch Case
- Loops

## 🎯 Purpose
This project was created to practice:
- Structure handling
- Basic financial calculations
- Menu-driven program logic

## ▶ How to Run
1. Compile the program:
   gcc cashflow.c -o cashflow
2. Run:
   ./cashflow

---

👨‍💻 Developed by Ritheesh K
#include <stdio.h> #include <string.h> struct Transaction { char type[10]; char note[30]; float amount; }; int main() { struct Transaction t[100]; int choice, count = 0; float balance = 0; do { printf("\n--- CASH FLOW MANAGER ---\n"); printf("1. Add Income\n"); printf("2. Add Expense\n"); printf("3. View Transactions\n"); printf("4. View Balance\n"); printf("5. Exit\n"); printf("Enter your choice: "); scanf("%d", &choice); switch (choice) { case 1: strcpy(t[count].type, "Income"); printf("Enter income amount: "); scanf("%f", &t[count].amount); printf("Enter note: "); scanf("%s", t[count].note); balance += t[count].amount; count++; printf("Income added successfully!\n"); break; case 2: strcpy(t[count].type, "Expense"); printf("Enter expense amount: "); scanf("%f", &t[count].amount); printf("Enter note: "); scanf("%s", t[count].note); balance -= t[count].amount; count++; printf("Expense added successfully!\n"); break; case 3: printf("\n--- TRANSACTION LIST ---\n"); for (int i = 0; i < count; i++) { printf("%s | %s | ₹%.2f\n", t[i].type, t[i].note, t[i].amount); } break; case 4: printf("Current Balance: ₹%.2f\n", balance); break; case 5: printf("Thank you!\n"); break; default: printf("Invalid choice!\n"); } } while (choice != 5); return 0; }
