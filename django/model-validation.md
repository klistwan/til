# How do you validate a model before saving it to the database?

```python
class BaseModel(models.Model):
    
    def clean(self, *args, **kwargs):
        # add custom validation here
        super().clean(*args, **kwargs)

    def save(self, *args, **kwargs):
        self.full_clean()
        super().save(*args, **kwargs)
```

This isn't done by default because of [backwards compatibility](https://code.djangoproject.com/ticket/13100).

Reference: https://stackoverflow.com/a/18876223

