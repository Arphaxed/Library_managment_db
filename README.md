# Library_managment_db
# Library Management System Database

## Overview

This is a simple library management system database designed to manage books, authors, members, loans, librarians, and sections within a library. It helps to keep track of which books are available, which members have borrowed them, and the librarians responsible for managing the library's operations.

I created this project as part of a database design exercise to demonstrate my understanding of relational database concepts, foreign keys, and normalization. It also highlights how I manage relationships between entities such as books, authors, and members, while ensuring data integrity using foreign key constraints.

## Database Structure

### Tables

1. **Author**:
   - Stores information about authors like their name, birth date, and nationality.

2. **Book**:
   - Stores book details, including the title, genre, publication year, ISBN, and a reference to the author.

3. **Member**:
   - Contains information about the library members: their name, email, phone number, and membership date.

4. **Loan**:
   - Tracks the books borrowed by members. Each loan has a book ID, member ID, loan date, and return date.

5. **Librarian**:
   - Stores librarian details, such as name, hire date, and contact information. Librarians may be responsible for managing specific sections or books.

6. **Section**:
   - Defines different sections of the library (e.g., Fiction, Non-fiction) where books are categorized.

7. **BookSection**:
   - This is a join table to create a many-to-many relationship between books and sections. A book can be part of multiple sections, and each section can have multiple books.

### Relationships

- **Author → Book**: One author can write multiple books, and each book references one author.
- **Book → Loan**: A book can be loaned multiple times, and each loan is associated with a book.
- **Member → Loan**: Each loan is linked to a member who borrowed the book.
- **Librarian → Loan**: A librarian can be responsible for managing specific loans (optional relationship).
- **Book → Section**: Books are assigned to sections, and each book can belong to multiple sections.

## Setup Instructions

1. **Create the Database**:

   To set up the database, start by creating the database in MySQL:
   ```sql
   CREATE DATABASE IF NOT EXISTS LibraryDB;
   USE LibraryDB;

![Alt text](libraraydb_EER diagram.JPGg)

