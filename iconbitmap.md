Перед заголовком отображается иконка. По умолчанию это иконка пера. С помощью метода iconbitmap() можно задать любую другую иконку. Например, определим в одной папке с файлом приложения какой-нибудь файл с иконкой, допустип, он называется "favicon.ico" и используем его для установки иконки
```python
def iconbitmap(self, bitmap=None, default=None):
		"""Установите для виджета со значком BITMAP значение BITMAP. Возвращать
		
		растровое изображение, если оно не задано.
		
		
		
		В Windows для установки значка можно использовать параметр ПО УМОЛЧАНИЮ
		
		для виджета и любых его потомков, у которых нет установленного значка
		
		явно. ПО умолчанию может быть указан относительный путь к файлу .ico
		
		(пример: root.iconbitmap(по умолчанию='myicon.ico'))."""

        if default:

            return self.tk.call('wm', 'iconbitmap', self._w, '-default', default)

        else:

            return self.tk.call('wm', 'iconbitmap', self._w, bitmap)
```

Также есть возможность использовать иконку без файла
```python
import tempfile, base64, zlib

ICON = zlib.decompress(base64.b64decode("eJxjYGAEQgEBBiDJwZDBysAgxsDAoAHEQCEGBQaIOAg4sDIgACMUj4JRMApGwQgF/ykEAFXxQRc="))

_, ICON_PATH = tempfile.mkstemp()

with open  (ICON_PATH,   "wb") as icon_file:

    icon_file.write(ICON)

root = Tk()

root.title("Hello METANIT.COM")

root.geometry("300x250")

root.iconbitmap(default=ICON_PATH)

root.mainloop()
```