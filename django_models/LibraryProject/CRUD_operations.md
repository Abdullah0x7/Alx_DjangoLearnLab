# CRUD Operations with Django Shell

```This document records the standard Create, Retrieve, Update, and Delete (CRUD) operations performed on the `Book` model using the Django shell.```

## 1. Create
**Objective:** Create a new book instance for "1984" by George Orwell.

```python
from bookshelf.models import Book

# Command to create the book
book = Book.objects.create(title="1984", author="George Orwell", publication_year=1949)

# Expected Output:
# <Book: 1984>

# Command to retrieve the book
t = Book.objects.get(title="1984")

# Command to display its details
print(t.title, t.author, t.publication_year)

# Expected Output:
# 1984 George Orwell 1949

# Command to fetch the book
book = Book.objects.get(title="1984")

# Update the title
book.title = "Nineteen Eighty-Four"

# Save the changes to the database
book.save()

# Verify the update
print(book.title)

# Expected Output:
# Nineteen Eighty-Four

# Command to fetch the updated book
book = Book.objects.get(title="Nineteen Eighty-Four")

# Delete the instance
book.delete()

# Expected Output:
# (1, {'bookshelf.Book': 1})
# The object is removed.

# Verification:
# Book.objects.all()
# Expected Output: <QuerySet []> (Empty list if this was the only book)