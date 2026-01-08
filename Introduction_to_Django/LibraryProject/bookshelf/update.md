Command:
book = Book.objects.get(title="1984")
book.title = "Nineteen Eighty-Four"
book.save()

Output:
# Nineteen Eighty-Four
# Expected output: The title is updated in the database.