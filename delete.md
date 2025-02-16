book = Book.objects.get(title="Nineteen Eighty-Four")
book.delete()

# Try to retrieve books again

books = Book.objects.all()
print(list(books)) # Expected Output: []
