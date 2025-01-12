# python.io

Ctrl+Alt+N запуск код runner для запуска файла пайтон для PyCharm
Shiry+F10 запуск код runner для запуска файла пайтон для vs code

Alt+Shift + + увеличение шрифта в PyCharm


При запуске кода через терминал, должны быть активны <string>>>> </string> это сообщает, что интерпретатор пайтон активен

Если просто пишутся выражения, то результат не будет видно и интерпретатор не отображает результат

## Самое важное в Python

<i style="color: red;">PYTHON</i> - объектно-ориентированный язык программирования

<i style="color: red;">ВСЕ СУЩНОСТИ В PYTHON - ОБЪЕКТЫ</i> 

<i style="color: #FC6C76;">Объект</i> - это экземпляр <i style="color: #2AA1CA;">класса</i>

<i style="color: #2AA1CA;">Класс</i> - это шаблон или прототип для создания объектов

На основании одного <i style="color: #2AA1CA;">класса</i> можно создавать много <i style="color: #FC6C76;">объектов</i>

У каждого объекта есть <i style="color: #FC6C76;">атрибуты</i>

Атрибут объекта называется <i style="color: #2AA1CA;">методом</i>, если его значение - <i style="color: #FC6C76;">функция</i>
## Основные типы

<i style="color: #1CAB9C">Строка</i> - str - 'Artem'
<i style="color: #1CAB9C">Целое число</i> - int - 10
<i style="color: #1CAB9C">Логический</i> - bool - <i style="color: #2AA1CA;">True, False</i>
<i style="color: #1CAB9C">Список</i> - list [1, 2, 3] 

> Желательно проставлять пробел после запятой. Перед и после закрывающими скобками этого можно не делать

<i style="color: #1CAB9C">Словарь</i>  - dict {'min': 5, 'max': 8}

>Словарь состоит с пары значений, которые в свою очередь состоят с ключей и значений


## Практика в интерактивном интерпретаторе Python

Использовать можно как одинарные. как и двойные кавычки, но лучше одинарные, дабы выработать синтаксис для читабельности кода

```
>>> 'Artem'
'Artem'
>>> 8
8
>>> 2+"
  File "<python-input-2>", line 1
    2+"
      ^
SyntaxError: unterminated string literal (detected at line 1)
>>> 2+2
4
>>> 2/1
2.0
>>> True
True
>>> False
False
>>> [1, 'abc', True]
[1, 'abc', True]
>>> {"name": 'Artem'}
{'name': 'Artem'} - /*происходит форматирование
>>>
```

## Встроенные функции

Пропишем вызов функции со строенной функцией
<i style="color: green">print</i> ('Hello Python')

<i style="color: green">print</i>  - *Встроенная функция*
('Hello Python') - *Вызов функции, значения типа str*

С помощью встроенной функции *def* можно создавать свои функции

### 1. print()

**Функция print() в Python** **используется для вывода текстовой информации на экран или в консоль**. Она может принимать один или несколько аргументов, одним из обязательных является строка или объект, который будет выведен.

```python
>>> print(-5.6)
-5.6 
```

### 2. input()

**Функция input()** — основной способ получения данных от пользователя в Python. Она запрашивает у пользователя ввод и возвращает введённое значение в виде строки.

```python
>>> name = input("Введите ваше имя: ")
print(name)
```

>Введите ваше имя: Артем
 Артем - значение str
 
### 3. **dir()

**dir() в Python** — **встроенная функция, которая возвращает список всех атрибутов и методов объекта**. [1](https://proghunter.ru/articles/pythons-dir-function-object-reference)

**Синтаксис**: dir([object]), где object — необязательный параметр. Если объект не указан, то функция возвращает список всех идентификаторов в текущей локальной области видимости.

```python
>>> name = 'Artem'  
print(dir(name))
```

#### Магические методы

>['__add__', '__class__', '__contains__', '__delattr__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__getitem__', '__getnewargs__', '__getstate__', '__gt__', '__hash__', '__init__', '__init_subclass__', '__iter__', '__le__', '__len__', '__lt__', '__mod__', '__mul__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__rmod__', '__rmul__', '__setattr__', '__sizeof__', '__str__', '__subclasshook__' ]

#### Методы преобразования и работы с содержимым вывода функции 

>['capitalize', 'casefold', 'center', 'count', 'encode', 'endswith', 'expandtabs', 'find', 'format', 'format_map', 'index', 'isalnum', 'isalpha', 'isascii', 'isdecimal', 'isdigit', 'isidentifier', 'islower', 'isnumeric', 'isprintable', 'isspace', 'istitle', 'isupper', 'join', 'ljust', 'lower', 'lstrip', 'maketrans', 'partition', 'removeprefix', 'removesuffix', 'replace', 'rfind', 'rindex', 'rjust', 'rpartition', 'rsplit', 'rstrip', 'split', 'splitlines', 'startswith', 'strip', 'swapcase', 'title', 'translate', 'upper', 'zfill']

У каждого объекта есть атрибуты и названия этих атрибутов, можно вывести путём функции dir. Как видно выше, *dir* отобразила имена всех атрибутов объекта

Для использования атрибута в методе прописываем 

```python
>>> name = 'Artem'  
print(name.upper())
```
 ARTEM преобразование вывода строки в верхний регистр
Если вывести значение имени после вывода атрибута, то значение не изменится
```python
>>> name = 'Artem'  
print(name)
```
Artem


### 4. type()

**type() в Python** — это **встроенная функция, которая в зависимости от переданных аргументов возвращает тип объектов или объект нового типа**. [1](https://pythonist.ru/funkcziya-type-v-python/)

**Если передаётся один аргумент**, type() возвращает тип переданного в неё объекта. **Когда передаются три аргумента**, функция возвращает объект нового типа. [1](https://pythonist.ru/funkcziya-type-v-python/)


``` python
x = 5
print(type(x))  # <class 'int'>
```

### 5. id()

**id() в Python** **возвращает уникальный идентификатор переданного ей в качестве аргумента объекта**. Этот идентификатор является адресом в памяти, по которому расположен сам объект. [1](https://ru.hexlet.io/qna/python/questions/chto-takoe-funktsiya-id-v-python)

**Синтаксис**: id(object). [2](https://realpython.com/ref/builtin-functions/id/)

**Функция принимает один параметр**: объект — может быть классом, переменной, списком, кортежем, набором и т. д.. [3](https://letpy.com/handbook/builtins/id/)

**Возвращаемое значение**: идентификатор объекта (уникальное целое число для данного объекта). [3](https://letpy.com/handbook/builtins/id/)

```python
name = 'Artem'  
print(id(name)) #1630813040736
```
### 6. len()

**len() в Python** — это **встроенная функция, которая возвращает количество элементов в объекте**, таком как списки, строки, кортежи и другие коллекции. [1](https://sky.pro/wiki/python/funkciya-len-v-python-poluchenie-dliny-spiska/)

Аргументом может быть последовательность (например, строка, байты, кортеж, список или диапазон) или коллекция (например, словарь, множество или замороженное множество). [2](https://docs.python.org/3/library/functions.html)

**Некоторые примеры использования функции len()**:

- определение количества элементов в списке, кортеже или множестве; [3](https://realpython.com/ref/builtin-functions/len/)
- подсчёт количества символов в строке; [3](https://realpython.com/ref/builtin-functions/len/)
- расчёт количества пар ключ-значение в словаре; [3](https://realpython.com/ref/builtin-functions/len/)
- явная проверка, пуст ли контейнер (для этого нужно сравнить len() с 0). [3](https://realpython.com/ref/builtin-functions/len/)

Функция len() не может быть применена к объектам, которые не поддерживают понятие длины. Например, попытка передать в len() число вызовет ошибку. [1](https://sky.pro/wiki/python/funkciya-len-v-python-poluchenie-dliny-spiska/)

```python
name = 'Artem'  
print(len(name)) #5
```

### 7. sum()
**sum() в Python** — **встроенная функция для суммирования элементов итерируемых объектов**, таких как списки, кортежи и множества. [1](https://sky.pro/wiki/python/funkciya-sum-v-python-summa-elementov-spiska/)

**Синтаксис**: sum(iterable, /, start=0). [2](https://letpy.com/handbook/builtins/sum/)[3](https://ru.hexlet.io/qna/python/questions/kakaya-funktsiya-nuzhna-dlya-slozheniya-chisle-v-python)

**Параметры**:

- **iterable** — объект, поддерживающий итерацию по его элементам. Ожидается, что элементы этого объекта являются числами, но не строками. Если объект пуст, функция вернёт начальное значение (start). [2](https://letpy.com/handbook/builtins/sum/)
- **start** (необязательный) — начальное значение суммы. По умолчанию равно 0. [1](https://sky.pro/wiki/python/funkciya-sum-v-python-summa-elementov-spiska/)

**Возвращаемое значение** — сумма начала и элементов данной итерации. [2](https://letpy.com/handbook/builtins/sum/)

```python
numbers = [1, 2, 3, 4, 5]  
total = sum(numbers)  
print(total)  # Вывод: 15 (сумма всех чисел в списке)
```
