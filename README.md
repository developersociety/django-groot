<img alt="Groot" align="right" src="https://cloud.githubusercontent.com/assets/448775/18818105/10d88b0c-8369-11e6-8155-b3c18b617c7c.png">
# Django Groot

[django-guardian]: https://github.com/django-guardian/django-guardian
[pip]: https://pip.pypa.io/

[django-guardian]. Groot requires django-guardian for maintaining permissions,
however Groot only focuses on groups for object permissions - per user object
level permissions aren't allowed for simplicity.

Groot is named after a team discussion about the best 'guardian' in the galaxy!

>>>>>>> Tidy markdown
## Installation

Using [pip]:

```console
$ pip install django-groot
```

<<<<<<< d87862183c913cb26ffd269bb2553586536b3424
Follow the instructions for installing `[django-guardian]` if you haven't
=======
Follow the instructions for installing [django-guardian] if you haven't
>>>>>>> Tidy markdown
already.

Edit your Django project's settings module, and add ``groot``:

```python
INSTALLED_APPS = [
    # ...
    'groot',
]
```

Usage
-----

Add `GrootAdminMixin` to the admin class you want Groot to be used on:

```python
from django.contrib import admin
from groot.admin import GrootAdminMixin

from .models import Post


@admin.register(Post)
class PostAdmin(GrootAdminMixin, BasePageAdmin):
    pass
```
