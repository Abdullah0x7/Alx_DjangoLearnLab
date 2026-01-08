Command:
book = Book.objects.get(title="Nineteen Eighty-Four")
book.delete()

Output:
# (1, {'bookshelf.Book': 1})
# Expected output: The book is deleted. Retrieving all books will show an empty QuerySet [].