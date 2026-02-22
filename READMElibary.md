# 📚 Library Management System (Python)

## 📌 Description

This project is a **simple library management system written in Python**, using **Object-Oriented Programming (OOP)**.

It allows a library to:
- store books and members,
- register members,
- allow members to borrow books,
- enforce basic borrowing rules.

This project is intended for **educational purposes**, to practice classes, object relationships, and basic business logic.

---

## 🧱 Class Overview

### `Library`

Represents a library.

#### Attributes
- `name`: name of the library
- `books`: list of books available in the library
- `members`: list of registered members

#### Methods
- `add_book(book)`: adds a book to the library
- `add_member(member)`: registers a new member
- `borrow_book(member_id, book_id)`: allows a member to borrow a book if conditions are met

---

## 🔄 Borrowing Logic

A book can be borrowed only if:
- the member exists,
- the book exists and is **available**,
- the member has borrowed **fewer than 3 books**.

When a book is borrowed:
- the book status is changed to `"borrowed"`,
- the book is added to the member’s `borrowed_books` list.

If any condition fails, the borrowing request returns `False`.

---

## ▶️ Example Usage

```python
library = Library("City Library")

library.add_member(member)
library.add_book(book)

success = library.borrow_book(member_id=1, book_id=101)

if success:
    print("Book borrowed successfully")
else:
    print("Borrowing failed")
