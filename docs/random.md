# Модуль random (генерация случайных чисел)

Для генерации случайных чисел необходимо подключить модуль `random`:

```python
import random
```

- `random.random()` - возвращает случайное дробное число в диапазоне от 0 до 1
- `random.randint(a, b)` - возвращает случайное число в диапазоне от `a` до `b`
- `random.choice(x)` - возвращает случайный элемент объекта x

```python
>>> import random
>>> random.random()
0.9094052716455632
>>> random.randint(1, 5)
5
>>> x = ['a', 'b', 'c']
>>> random.choice(x)
'c'
```

