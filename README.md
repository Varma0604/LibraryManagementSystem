# LibraryManagementSystem
# Library Management System

This repository contains the SQL scripts for a simple Library Management System. It includes scripts for creating the database schema and inserting sample data.

## Database Schema

The database schema includes the following tables:
- Authors
- Genres
- Books
- Members
- Transactions

The `schema.sql` file contains the SQL statements to create these tables.

## Sample Data

The `data.sql` file contains sample data to populate the tables.

## Usage

To set up the database:

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/LibraryManagementSystem.git


   List All Books and Their Authors:
   SELECT Books.Title, Authors.Name AS Author
    FROM Books
    JOIN Authors ON Books.AuthorID = Authors.AuthorID;

Find Available Copies of a Specific Book:
SELECT Title, AvailableCopies
FROM Books
WHERE Title = '1984';

List All Overdue Books (Assuming a 14-Day Borrowing Period)
SELECT Members.Name, Books.Title, Transactions.BorrowDate
FROM Transactions
JOIN Members ON Transactions.MemberID = Members.MemberID
JOIN Books ON Transactions.BookID = Books.BookID
WHERE Transactions.ReturnDate IS NULL AND Transactions.BorrowDate < CURRENT_DATE - INTERVAL '14 days';



   
   


   
