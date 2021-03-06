## Avatar Field
Avatar Field is a simple Django field that helps you to add avatar icon beside name in choice for ForeignKey field.

  
Quick start
-----------

 1. `pip install django-avatarfield`

 2. Add "avatar_field" to your INSTALLED_APPS setting like this.

    ```python
	INSTALLED_APPS = [
		...
		'avatar_field',
		]
	```

 3. Use AvatarForeignKey instade of django normal ForeignKey and add image_field to tell the app what should use from the relation model.
```python
from avatar_field.model_fields import AvatarForeignKey

class Person(models.Model):
	user = AvatarForeignKey("User", on_delete=models.CASCADE, image_field='picture')
```

 4. Run `python manage.py makemigration` to create the migrations.
 5. Run `python manage.py migrate` to reflact it on the database.

Now, all you need to go to the dashboard and see.

![trying it](https://im7.ezgif.com/tmp/ezgif-7-e1f58bb62755.gif)
