# События, метод bind

При взаимодействии пользователя с приложением возникают различные события (нажата кнопка мыши, нажата клавиша на клавиатуре, пользователь перемещает курсор мыши).

### Обработка событий

Обработать события (т.е. вызвать определённую функцию при настпулении определённого события) можно с помощью метода `bind`:

```python
component.bind(event, function)
```

`component` - компонент, с которым происходит действие, `event` - событие, `function` - вызываемая функция.

### События

| Событие                 | Описание                               |
| ----------------------- | -------------------------------------- |
| &lt;Button-1&gt;        | Нажатие кнопки мыши                    |
| &lt;B1-Motion&gt;       | Движение мыши с зажатой кнопкой мыши   |
| &lt;ButtonRelease-1&gt; | Отпускание нажатой кнопки мыши         |
| &lt;Double-Button-1&gt; | Двойной клик                           |
| &lt;Triple-Button-1&gt; | Тройной клик                           |
| &lt;Motion&gt;          | Движение мыши                          |
| &lt;Enter&gt;           | Курсор мыши наведён на компонент       |
| &lt;Leave&gt;           | Курсор мыши покинул область компонента |
| &lt;Key&gt;             | Нажатие любой клавиши на клавиатуре    |
| q                       | Нажатие клавиши q                      |
| &lt;KeyRelease&gt;      | Отпускание нажатой клавиши             |
| &lt;Return&gt;          | Нажатие клавиши Enter                  |

При указании событий мыши цифрой обозначается кнопка: 1 - левая, 2 - средняя (колёсико мыши), 3 - правая.

### Параметр event

В функцию, вызываемую методом `bind`, передаётся аргумент `event`, который содержит информацию о событии (например, координаты мыши).

#### Событие мыши

Пример с событием мыши:

```python
from tkinter import *

class WindowApplication:
    def __init__(self):
        self.root = Tk()
        self.root.bind('<Motion>', self.mouseMove)
        self.root.mainloop()

    def mouseMove(self, event):
        print(event)

WindowApplication()
```

При движении мыши будет отображаться информация о событии:

```python
<Motion event state=Mod1 x=179 y=7>
<Motion event state=Mod1 x=178 y=8>
<Motion event state=Mod1 x=177 y=9>
```

Координаты можно получить следующим образом: `event.x`, `event.y`.

#### Событие клавиатуры

Пример с событием клавиатуры:

```python
from tkinter import *

class WindowApplication:
    def __init__(self):
        self.root = Tk()
        self.root.bind('<Key>', self.keyPress)
        self.root.mainloop()

    def keyPress(self, event):
        print(event)

WindowApplication()
```

При нажатии клавиши будет отображаться информация о событии:

```python
<KeyPress event state=Mod1 keysym=q keycode=81 char='q' x=285 y=329>
```

`event.keysym` - буквенный код клавиши (например, space - пробел), `event.keycode` - код клавиши, `event.char` - символ.
