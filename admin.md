# Registrar un modelo
````
from django.contrib import admin
from .models import Cart, CartItem

admin.site.register(Cart)
admin.site.register(CartItem)
````

# Registrar un modelo 2
````
from django.contrib import admin
from .models import Category


class CategoryAdmin(admin.ModelAdmin):
    name = 'apps.category'
    prepopulated_fields = {'slug': ('category_name', )}
    list_display = ('category_name', 'slug')


# Register your models here.
admin.site.register(Category, CategoryAdmin)
````
