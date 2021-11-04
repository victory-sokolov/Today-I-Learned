# Circular imports for Type hints


```python
# models.py

from controllers import BookController

class Book:
    ...

    def get_controller(self) -> BookController:
        return BookController(self)
```

```
# controller.py

from __future__ import annotations

from typing import TYPE_CHECKING

if TYPE_CHECKING:
    from models import Book


class BookController:
    def __init__(self, book: Book) -> None:
        self.book = book
```
