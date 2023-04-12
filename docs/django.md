## Django Cheat Sheet

### Django Admin Panel

#### Displaying a `table` in `tabular` form and apply default sorting

```
from django.contrib import admin

from .models import Question


class QuestionAdmin(admin.ModelAdmin):
    list_display = ("full_name", "email", "phone_number", "speciality", "time", "request_date")
    ordering = ("request_date",)


admin.site.register(Question, QuestionAdmin)
```
