[Ориг документация](https://docs.python.org/3/library/tkinter.html)
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

### Иконка приложения [[iconbitmap]],[[iconphoto]]
```python
root.iconbitmap(default="путь_к_файлу/название_файла.ico")
```

```python 
icon = PhotoImage(file = "название_файла.png")
root.iconphoto(False, icon)
```

### Перехват закрытия окна
```python
def finish():

    root.destroy()  # ручное закрытие окна и всего приложения

    print("Закрытие приложения")`

root = Tk()

root.geometry("250x200")

root.title("Hello METANIT.COM")

root.protocol("WM_DELETE_WINDOW", finish)

root.mainloop()
```
