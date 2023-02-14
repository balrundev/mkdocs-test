# Функции

Объявление функции:

```python
def function_name(args):
    ...
```

Функция с возвращаемым значением:

```python
def function_name(args):
    ...
    return ...
```

Примеры:

```python
def sayHello(name):
    print(f'Hello, {name}!')

sayHello('User') # вывод: Hello, User!
```

```python
def avg(data):
    return sum(data) / len(data)

x = [1, 2, 3, 4, 5]
print(avg(x)) # вывод: 3.0
```


