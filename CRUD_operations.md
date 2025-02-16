# CRUD Operations in Django Shell

## Create a Book

```python
from bookshelf.models import Book

book = Book.objects.create(title="1984", author="George Orwell", publication_year=1949)
print(book)  # Expected Output: 1984

```

## Retrieve the Book

book = Book.objects.get(title="1984")
print(book.title, book.author, book.publication_year)

# Expected Output: 1984 George Orwell 194

## Update the Book

book = Book.objects.get(title="1984")
book.title = "Nineteen Eighty-Four"
book.save()

updated_book = Book.objects.get(id=book.id)
print(updated_book.title) # Expected Output: Nineteen Eighty-Four

## Delete the Book

book = Book.objects.get(title="Nineteen Eighty-Four")
book.delete()

books = Book.objects.all()
print(list(books)) # Expected Output: []
