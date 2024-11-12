# Admin Configuration for Book Model

## Objective
Gain practical experience with the Django admin interface by configuring the admin to manage the Book model.

## Steps Taken

### 1. Register the Book Model with the Django Admin
- Opened `bookshelf/admin.py`.
- Imported the `Book` model.
- Registered the `Book` model with the admin site using `admin.site.register(Book)`.

### 2. Customize the Admin Interface
- Created a custom admin class `BookAdmin` that inherits from `admin.ModelAdmin`.
- Configured the following:
  - **list_display**: Displayed `title`, `author`, and `publication_year`.
  - **list_filter**: Added filters for `author` and `publication_year`.
  - **search_fields**: Enabled search for `title` and `author`.

### Final Code in `admin.py`
```python
from django.contrib import admin
from .models import Book

class BookAdmin(admin.ModelAdmin):
    list_display = ('title', 'author', 'publication_year')
    list_filter = ('author', 'publication_year')
    search_fields = ('title', 'author')

admin.site.register(Book, BookAdmin)