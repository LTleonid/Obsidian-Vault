## Начало:
```python
#Импорт библиотек
from tkinter import *
from tkinter import ttk
#Краткая функция в переменной
root = Tk()
#Зациклевание работы приложения
root.mainloop()
```
## Для окна приложения:

### Название окна
```python 
root.title('Название окна приложения')
```
### Размеры окна
```python
root.geomtry('100x100')   # ширина x высота
```

Минимальные и максимальные размеры
```python
root.minsize(Ширина,Высота)    # минимальные размеры

root.maxsize(Ширина,Высота)    # максимальные размеры
```

### Растягивание окна
```python
root.resizable(False, False) #По ширине, По высоте
```

### Иконка окна [[iconbitmap]], [[iconphoto]]
```python
root.iconbitmap(default="путь до файла/название файла.ico") 
```

sadasd