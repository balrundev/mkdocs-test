# Списки (lists)

Список - это упорядоченный и изменяемый набор объектов любых типов.

```python
numbers = [1, 2, 3, 4, 5]
```

### Добавление элемента в список

```python
>>> numbers.append(100)
>>> numbers
[1, 2, 3, 4, 5, 100]
```

### Обращение к элементу списка

```python
>>> numbers[0]
1
```

### Изменение элемента списка

```python
>>> numbers[1] = 150
>>> numbers
[1, 150, 3, 4, 5]
```

*Нумерация индексов начинается с нуля.*

### Удаление элемента списка

```python
>>> del numbers[1]
>>> numbers
[1, 3, 4, 5]
```

### Другие операции

- `len(values)` - возвращает длину списка
- `values.extend(data)` - добавление элементов списка data в конец списка values
- `values.copy()` - возвращает копию списка
- `values.clear()` - очистка списка
- `values.count(x)` - возвращает количество элементов со значением x
- `values.index(x)` - возвращает индекс первого элемента со значением x (если такого элемента нет, поднимается исключение **ValueError**)

