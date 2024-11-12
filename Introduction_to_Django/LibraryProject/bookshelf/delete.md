# Delete Operation

Command:
```python
from bookshelf.models import Book

retrieved_book.delete()
books = Book.objects.all()
print(books)

# Expected Output
# An empty queryset is returned, confirming that the book has been deleted.