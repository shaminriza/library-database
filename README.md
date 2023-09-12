# Library Management System Database and Stored Procedures

## Overview

This repository contains SQL code for creating a Library Management System database schema and populating it with sample data. Additionally, it includes a set of stored procedures to query and retrieve information from the database.

## Database Schema

The database schema consists of several tables, including `tbl_publisher`, `tbl_book`, `tbl_library_branch`, `tbl_borrower`, `tbl_book_loans`, `tbl_book_copies`, and `tbl_book_authors`. These tables represent various aspects of the library system, such as publishers, books, branches, borrowers, loans, book copies, and authors.

## Populating the Database

To create the database and populate it with sample data, you can execute the provided SQL script. The script includes INSERT statements to add sample records to the tables, such as publishers, books, branches, borrowers, loans, book copies, and authors.

## Stored Procedures

The repository includes several stored procedures designed to retrieve specific information from the database. Here is a brief description of each stored procedure:

1. `bookCopiesAtAllSharpstown`: Retrieves the number of copies of a specified book owned by the "Sharpstown" branch.

2. `bookCopiesAtAllBranches`: Retrieves the number of copies of a specified book owned by each library branch.

3. `NoLoans`: Retrieves the names of borrowers who do not have any books checked out.

4. `LoanersInfo`: Retrieves information about books loaned out from a specified branch with a due date matching the current date, including book title, borrower's name, borrower's address, date out, and due date.

5. `TotalLoansPerBranch`: Retrieves the branch name and the total number of books loaned out from each library branch.

6. `BooksLoanedOut`: Retrieves the names, addresses, and the number of books checked out for borrowers with more than a specified number of books checked out.

7. `BookbyAuthorandBranch`: Retrieves titles and the number of copies owned by a library branch for books authored by a specified author and located in a specified branch.

## Usage

To execute any of the stored procedures, you can use a SQL database management tool or run the SQL queries directly. Ensure that you have the database schema and sample data in place before executing the procedures.

```sql
-- Example: Executing the bookCopiesAtAllSharpstown procedure
EXEC dbo.bookCopiesAtAllSharpstown;
