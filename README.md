# Installation

Install using pip:

```shell
pip install git+https://github.com/nezhar/django-model-prefix@main
```

Add model_prefix to your INSTALLED_APPS list. Make sure it is the first app in the list

```python
INSTALLED_APPS = [
    'django_db_prefix',
    ...
]
```

# Usage

## Global table prefix

The global database table prefix can be configured using the `DB_PREFIX` setting

```python
DB_PREFIX = "foo_"
```

## Model table prefix

Optionally a model based prefix can also be defined by extending the models meta class

```python
class Meta:
    db_prefix = "bar_"
```

This can be also used in order to disable the global prefix for a specific model


```python
class Meta:
    db_prefix = None
```
