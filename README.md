# Python

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
 
### 3. dir()

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

### 8. round()
**round()** — **встроенная функция в Python для округления чисел**. [1](https://skillbox.ru/media/code/okruglenie-v-python-vybiraem-luchshiy-sposob/)[3](https://pythonru.com/uroki/funkcija-round-dlja-nachinajushhih)
**Синтаксис**: round(number, digits). В качестве первого аргумента (number) передаётся дробное число, а во втором (digits) указывается количество чисел после запятой. Второй аргумент по умолчанию равен нулю. [1](https://skillbox.ru/media/code/okruglenie-v-python-vybiraem-luchshiy-sposob/)

**Возвращаемое значение**: функция round() возвращает ближайшее целое число к заданному числу, если количество цифр не указано, или число, округлённое до указанного количества цифр, если оно указано. [2](https://letpy.com/handbook/builtins/round/)

**Алгоритм вычисления функции round() различается в разных версиях языка**:

- **В Python 2** за основу взяты классические правила арифметики: 1, 2, 3, 4 после запятой ведут к округлению в меньшую сторону, а 5, 6, 7, 8, и 9 — в большую. Например: 7,6 → 8 — округление в большую сторону, 7,4 → 7 — округление в меньшую сторону. [1](https://skillbox.ru/media/code/okruglenie-v-python-vybiraem-luchshiy-sposob/)
- **В Python 3** используется так называемый «банковский» метод, то есть округление до ближайшего чётного числа: 3,5 → 4, 6,5 → 6. 

```python
>>> round(6.4457, 2)
6.45
>>>
```

### 9. min

**Функция min() в Python возвращает элемент с наименьшим значением** из переданных в функцию данных. [1](https://letpy.com/handbook/builtins/min/)

**Параметры**:

- **iterable** — итерируемый объект, такой как список, кортеж, набор, словарь и т. д.; [1](https://letpy.com/handbook/builtins/min/)[3](https://pythonstart.ru/osnovy/min-max-python)
- ***iterables** (необязательно) — любое количество итераций, может быть более одного; [3](https://pythonstart.ru/osnovy/min-max-python)
- **key** (необязательно) — ключевая функция, в которую передаются итерации, а сравнение выполняется на основе возвращаемого значения; [1](https://letpy.com/handbook/builtins/min/)[3](https://pythonstart.ru/osnovy/min-max-python)
- **default** (необязательно) — значение по умолчанию, если данный итерируемый объект пуст. [1](https://letpy.com/handbook/builtins/min/)[3](https://pythonstart.ru/osnovy/min-max-python)

```python
number = [7, 3, 8, 5, 1, 6]  
smallest_number = min(number)  
print("Наименьшее число:", smallest_number) # 1
```

### 10. Max

**Функция max() в Python возвращает самый большой элемент в итерируемом объекте**. Её также можно использовать для поиска самого большого элемента между двумя или более параметрами. [1](https://pythonstart.ru/osnovy/min-max-python)

**Некоторые параметры функции**:

- **iterable** — итерируемый объект, такой как список, кортеж, словарь или строка. [3](https://realpython.com/ref/builtin-functions/max/)
- **default** — значение по умолчанию, если итерируемый объект пуст. [1](https://pythonstart.ru/osnovy/min-max-python)[3](https://realpython.com/ref/builtin-functions/max/)
- **key** — ключевая функция, в которую передаются итерации, и выполняется сравнение на основе её возвращаемого значения. [1](https://pythonstart.ru/osnovy/min-max-python)
Функция max() универсальна и может работать с различными типами данных, включая числа и строки. [3](https://realpython.com/ref/builtin-functions/max/)

```python
number = [7, 3, 8, 5, 1, 6]  
maxtest_number = max(number)  
print("Наибольшее число:", maxtest_number) #8
```

### 11. int()
**Int в Python** — это **тип данных, представляющий целые числа** вида 0, 1 или 10. [1](https://practicum.yandex.ru/blog/tipy-dannyh-v-python/) В Python целыми числами являются все числа, которые лишены дробной части, то есть не имеют плавающей точки. [2](https://timeweb.com/ru/community/articles/chisla-v-python-i-metody-raboty-s-nimi)

Для преобразования значений в целые числа в Python используется **встроенная функция int()**. [3](https://letpy.com/handbook/builtins/int/)[4](https://ru.hexlet.io/qna/python/questions/chto-delaet-funktsiya-int-v-python) Она принимает два параметра: [3](https://letpy.com/handbook/builtins/int/)

1. **value** — любая числовая строка, байтовый объект или число. [3](https://letpy.com/handbook/builtins/int/)
2. **base** (необязательный) — система счисления, в которой в данный момент находится значение. [3](https://letpy.com/handbook/builtins/int/)

Если передать функции целое число, то она вернёт его же. Если передать вещественное (дробное) число, то оно будет округлено до целого в сторону нуля (отбрасывая дробную часть). Функция int(), вызванная без аргументов, вернёт 0. [4](https://ru.hexlet.io/qna/python/questions/chto-delaet-funktsiya-int-v-python)

### 12. str()

**Str в Python** — это **встроенный тип данных, который используется для представления и оперирования строками текста**. Строка представляет собой последовательность символов, таких как буквы, цифры, символы пунктуации и другие специальные символы. [1](https://otvet.mail.ru/question/235019130)
Строки в Python могут быть заключены в одинарные (') или двойные (") кавычки, и обе формы эквивалентны. [1](https://otvet.mail.ru/question/235019130)

**Str поддерживает множество методов** для работы со строками, таких как конкатенация (соединение строк), извлечение подстрок, поиск и замена подстрок, преобразование регистра и многие другие операции. [1](https://otvet.mail.ru/question/235019130)

**Строки в Python являются неизменяемыми**, что означает, что после создания строки её содержимое нельзя изменить. Вместо этого при операциях со строками создаются новые строки. [1](https://otvet.mail.ru/question/235019130)

### 13. bool()

**Bool в Python** — это **логический тип данных, который принимает два значения**: True (истина) и False (ложь). [1](https://pythonchik.ru/osnovy/logicheskiy-tip-dannyh)[2](https://tproger.ru/translations/truthy-and-falsy-values-in-python)

Этот тип данных полезен в программировании для управления порядком выполнения программы с помощью условных операторов, таких как if, else и elif, а также для управления циклами и другими структурами управления. [3](https://javarush.com/quests/lectures/ru.javarush.python.core.lecture.level04.lecture04)

**Для приведения других типов данных к булевому типу в Python используется функция bool()**. [1](https://pythonchik.ru/osnovy/logicheskiy-tip-dannyh) По умолчанию, любое ненулевое или непустое значение будет преобразовано в True, а нулевые или пустые значения — в False. [3](https://javarush.com/quests/lectures/ru.javarush.python.core.lecture.level04.lecture04)

**Пример использования**: числовое значение 0 или пустая строка всегда будет False, а ненулевые числа и непустые строки интерпретируются как True. [4](https://kedu.ru/press-center/articles/info-polnoe-rukovodstvo-po-funktsii-bool-v-python/)

### 14. dir()

**dir() в Python** — **встроенная функция, которая возвращает список всех атрибутов и методов объекта**. Она используется для получения справочной информации о любом объекте в Python, включая модули, функции, списки, словари, классы и экземпляры классов. [1](https://proghunter.ru/articles/pythons-dir-function-object-reference)

**Синтаксис функции**: dir([object]), где object — необязательный параметр. Если object не указан, то функция возвращает список всех идентификаторов в текущей локальной области видимости. [1](https://proghunter.ru/articles/pythons-dir-function-object-reference)

**При вызове без аргумента** dir() возвращает список переменных, доступных в локальной области. **Если передать функции объект**, она вернёт список атрибутов указанного объекта. [2](https://ru.hexlet.io/qna/python/questions/chto-takoe-funktsiya-dir-v-python)

## Отступы в коде PYTHON

За счёт отступов Python понимает код
Отступ равен 4ем пробелам

```python
def my_name(name):  
    print(name)  
my_name('Artem')
```
В данной записи вызвали функцию с переменной _name_, которая в свою очередь вывела имя

```python
def my_name(name):  
print(name)  
my_name('Artem')
#  путь", line 2
    print(name)
    ^^^^^
#IndentationError: expected an indented block after function definition on line 1

#Process finished with exit code 1
```

### Форматирование кода Python

<i style="color: #1CAB9C">PEP8</i> - документ, описывающий рекомендации по написанию кода Python

[Документация](https://peps.python.org/pep-0008 )

#### Некоторые выдержки из <i style="color: #1CAB9C">PEP8</i>

1. Для отступов использовать пробелы, а не _Tab_
2. Длина строк должна быть не более _79 символов_
3. _Функции_ и _классы_, должны быть отделены _двумя пустыми строками_
4. Импорты модулей должны быть на отдельных строках
5. _Комментарии в строки_ кода должны отделяться по крайней мере _2 пробелами_

```python
my_list =      [1, 2,    3]  
  
print(my_list)  #[1, 2, 3] - python проигнорировал лишние отступы и код отработал корректно, но писать нужно согласно рекомандациям

```

### Выражения (Expressions)

Результатом каждого _выражения_ является _значение_

```python
5 + 3   #8 - сумма значений
```

```python
a > b  # True или False
```

>Cравнивание значений 2х переменных

```python
'Hello' + 'World'  # 'Hello World' 
```

>Соединение 2х строк

```python
my_func(10, 5)   # результат функции
```

>Вызов функции



## Инструкции

_Инструкция_ выполняет _действие_

```python
my_name('Artem')   # Присвоения значения
```

```python
# Условная инструкция
if my_name:
    print(my_name)
```

```python
# Импортирование модуля
import datetime
```

```python
import datetime  
  
print(datetime.datetime.now())   # 2025-01-17 17:29:52.595815 вывели время в данную секунду
```

Чтобы узнать инструкцию, пропишем

```python
import datetime  
  
print(import datetime) # Expression expected - это означает, import является инструкцией
```

## Переменные

#### Имена в Python

>_snake_case_ - переменные, функции, методы, модули (часто используемые)

> _PascalCase_ - Классы

> _my-package_ - Пакеты (наборы модулей)

> _DB_PASSWORD_ - Константы


## Объявление переменных и присвоение им значения

```python
my_number = 10   # Правильность присвоения
```

_Python_ - язык с *динамической типизацией*, то бешь одной и той же переменной, можно присвоить разные значения

```python
my_variable = 10
my_variable = 'Artem'
my_variable = True
```

вывод значений переменных в терминал

```python
my_number = 10  
print(my_number)  #10
  
my_boolean = True  
print(my_boolean)  #True
```
## Динамическая типизация

```python
a = 10   # <class 'int'>
a = True   # <class 'bool'>
a = 'Artem'   # <class 'str'>
a = None   # <class 'NoneType'>
```

#### Рекомендации по работе с переменными

>Имя переменной должно отвечать на вопрос - _Что содержит?_
>Имя функции должно отвечать на вопрос - _Что выполняет или возвращает?_

1. Всегда выбирать осмысленные названия
2. В названиях переменных, использовать имя существительное _name_, _comments_, _new_photos_
3. Названия функций и методов начинать с глагола, например get_data(получить данные), create_request(создать запрос), merge_names(объединить имена)

## Типы и структуры данных

>В Python _отсутствуют_ примитивные типы

> В Python существуют _изменяемые (Mutable) и неизменяемые (Immutable) объекты_

Объект у которого тип _int_ является неизменяемым, например список, является изменяемым объектом, но при этом он остаётся в памяти

### Типы неизменяемых объектов

- string (строка) str
- boolean (логический) bool
- integer (целое число) int
- float (число с десятичной точкой)
- tuple (кортеж) tuple
- None (ничто) NoneType

### Типы изменяемых объектов

- list (список) list
- dictionary (словарь) dict
- set (набор) set
- user-defined classes (пользовательские классы)

## Переменные и объекты

_Переменная_ - это ссылка на определённый объект в памяти

Как можно узнать какую ссылку содержит переменная?

Для этого существует встроенная функция - _id_

```python
my_country = 'Country'  
print(id(my_country))  #3000249500848  адрес объекта в памяти
  
my_name = 'Artem'  
print(id(my_name))   #3000249501184 адрес объекта в памяти
```

> Переменные могут ссылаться на _один_ объект в памяти

```python
my_number = 10  
print(id(my_number))  #140731926512840
  
other_numder = my_number  
print(id(other_numder))   #140731926512840
```

## Строки

> _Строка_ - последовательность символов

_Одинарные кавычки_ в строке используют для написания строки в одно слово

_Двойные кавычки_ используют для написания нескольких слов в строке

>Нужно придерживаться одного стиля написания кода с кавычками

При создании строк, каждая строка - это экземпляр _str_

### Многострочные строки

```python
info_msg = """You are  
learning the easiest  
programing language - 
Python"""   # 3 двойных кавычки

print(info_msg)
#You are  
#learning the easiest  
#programing language -   
#Python
```

### Встроенные функции и строки

```python
my_name = 'Artem'  
print(len(my_name))  
  # 5 - число символов в строке
print(my_name[0])  
  # B - вывести символ строки по индексу
print(my_name[3:5])
#em - показать символы с индексами с 3 по 5
```

## Целые числа - _int_

```python
input_str = input("Введите число:")  
  
print(input_str)  # Введите число:10
  
print(type(input_str))   # <class 'str'>
```

Выполним конвертацию

Если делать конвертацию строки в число
```python
input_str = input("Введите число:")  #aaa
input_int = int(input_str)  
print(input_int)  
  print(type(input_int))
#Введите число:фис
#Traceback (most recent call last):
  #File "D:\Обучалка\Python\python\main.py", line 2, in <module>
#    input_int = int(input_str)
#ValueError: invalid literal for int() with base 10: 'фис'
```

Возведение в степень и тип переменной
```python
int_pow = pow(2, 3)  # 8
print(type(int_pow))  #<class 'int'>
```

## Числа с десятичной точкой - _float_

```python
average_price = 17.1  
  
print(average_price)  # 17.1
  
print(type(average_price)) # <class 'float'>
```

#### Конвертация чисел

```python
average_price = 17.12  
price = int(average_price)  #  конвертировали в целое число
print(type(price))  # <class 'int'>
print(price)  # 17
```

```python
str_temperature = '17.12'  
temperature = float(str_temperature)  # конвертировалb в десятичное число
print(type(temperature))   # <class 'float'>
print(temperature)  # 17.12
```

#### Округление до ближайшего целого числа - _int_

```python
average_price = 17.20  
print(round(average_price))   # 1 
```

```python
rate = 0.78  
print(round(rate))   # 1
print(type(round(rate)))   # <class 'int'>
```

## Комплексные числа - _complex_

> Комплексное число состоит из действительной и мнимой части

<strong style='color: #6ABDC8; text-align-center; margin: 0 auto: font-size: 30px'>Структура и синтаксис</strong>

Результат сложения
```python
complex_a = 10 +7j  
complex_b = 3 + 3j  
  
res = (complex_a + complex_b) 
print(res)   # (13+10j)
```

Результат умножения
```python
complex_a = 10 + 7j  
complex_b = 3 + 3j  
  
res = (complex_a * complex_b)  
print(res)  # (9+51j)
# (10 + 7j)(3 + 3J) = 30 + 30j + 21j - 21 = (9 + 51j)   +21j^2 превращается в -21
```

## Логический тип - _bool_

##### Структура и синтаксис

```python
is_autorised = True  
  
print(is_autorised)  # True
  
print(type(is_autorised))  #<class 'bool'>
```

<i style='color: #FE6B73;'>BOOl</i> часто используется при проверке правдивости выражения

Результаты выражений

```python
print(100 > 24)  #True
  
print(-5 > 0)  #False
  
print('Long string' > 'Long')  #True (выполняется посимновльное сравнение)

print('Long string' > 'Self')  #False (выполняется посимновльное сравнение)
  
print([1, 2, 3] == [1, 2, 3])   #True
```

Конвертация в _логическое_ значение

```python
bool(my_value)
^встроенная функция
```

```python
print(bool(10))    #True
print(bool('abc'))    #True
print(bool([]))    #False
print(bool([1, 2, 3]))  #True
print(bool({}))    #False
print(bool(None))   #False
print({'a': 1} == {'a': 2})   #False
print({'a': 1} == {'a': 1})    #True
```

## Конвертация типов

> Python _не выполняет неявную_ конвертацию типов значений

### Встроенные функции для _явной_ конвертации типов

1. str()
2. float()
3. tuple() 
4. int()
5. list()
6. set()

#### Операции с значениями разных типов

Соединим разные типы:

```python
print('10' + 5)


Traceback (most recent call last):
  File "D:\Обучалка\Python\python\main.py", line 1, in <module>
    print('10' + 5)
          ~~~~~^~~
TypeError: can only concatenate str (not "int") to str
```

```python
print(int('10') + 5)  # 15

print('10' + str(5))  # 105
```

Работая с разными типами, можем получить разные результаты, но используя типы числовые, можем получить результат без конвертаций

```python
int_num = 5   # 5.0 
float_num = 4.5   # 4.5
  
print(int_num + float_num)   #9.5 для оператора + вызывается магический метод равносильный записи ниже но результат
```

```python
print(int_num.__add__(float_num))   #NotImplemented
```

В методе __add__ не реализован функционал добавления к целому числу, числа с десятичной точкой
Метод  <i>__add__</i>класса int
Чтобы выполнить конвертацию, python автоматически конвертирует числа, добавляя метод __radd__ тем самым выполняя условие конвертации

```python
print(float_num.__radd__(int_num))   # 9.5
```

Метод  <i>__radd__</i> класса int

Соединим булево значение с целочисленным 

```python

bool_val = True  # 1
int_val = 7  
print(bool_val + int_val)  #8

```

## Магические методы

> _Магические методы_ - это внутренние методы классов и они обычно не вызываются явно

Узнаем какие атрибуты есть в определённом классе

```python
print(dir(bool))
```

>['__abs__', '__add__', '__and__', '__bool__', '__ceil__', '__class__', '__delattr__', '__dir__', '__divmod__', '__doc__', '__eq__', '__float__', '__floor__', '__floordiv__', '__format__', '__ge__', '__getattribute__', '__getnewargs__', '__getstate__', '__gt__', '__hash__', '__index__', '__init__', '__init_subclass__', '__int__', '__invert__', '__le__', '__lshift__', '__lt__', '__mod__', '__mul__', '__ne__', '__neg__', '__new__', '__or__', '__pos__', '__pow__', '__radd__', '__rand__', '__rdivmod__', '__reduce__', '__reduce_ex__', '__repr__', '__rfloordiv__', '__rlshift__', '__rmod__', '__rmul__', '__ror__', '__round__', '__rpow__', '__rrshift__', '__rshift__', '__rsub__', '__rtruediv__', '__rxor__', '__setattr__', '__sizeof__', '__str__', '__sub__', '__subclasshook__', '__truediv__', '__trunc__', '__xor__', 'as_integer_ratio', 'bit_count', 'bit_length', 'conjugate', 'denominator', 'from_bytes', 'imag', 'is_integer', 'numerator', 'real', 'to_bytes']

Не все магические методы используются для конвертации, ибо имеют определённую задачу, к примеру можем вывести документацию класса _bool_

```python
print(bool.__doc__)
```

>Returns True when the argument is true, False otherwise.
The builtins True and False are the only two instances of the class bool.
The class bool is a subclass of the class int, and cannot be subclassed.

>Возвращает значение True, если аргумент равен true, в противном случае значение False. Встроенные значения True и False являются единственными экземплярами класса bool. Класс book является подклассом класса int и не может быть разделен на подклассы.

Чтобы получить помощь по определённому магическому методу или атрибуту пропишем конструкцию

```python
my_list = []  
print(help(my_list.__eq__))

"""__eq__(value, /) unbound builtins.list method
    Return self==value.

None
"""
```

## Списки _LIST_

> Список - упорядоченная последовательность элементов

##### Структура и синтаксис

```python
my_fruits = ["apple", "banana", "cherry"]  #тип класса str
  
posts_ids = [345, 56, 34, 34]  # тип класса int
  
user_inputs = [True, '🤩', 'hi!', 10.5]   # джопускается разнотипность
```

> Порядок элементов в списке <u>имеет значение</u>

```python
my_fruits = ['apple', 'banana', 'cherry']  
other_fruits = ['apple', 'cherry', 'banana']  
print(my_fruits == other_fruits)   #False
```

```python
my_fruits = ['apple', 'banana', 'cherry']  
other_fruits = ['apple', 'banana', 'cherry']  
print(my_fruits == other_fruits)   #True
```

### Длина списка

```python
empty_list = []  
print(len(empty_list))    #0
my_fruits = ['apple', 'banana', 'cherry']  
print(len(my_fruits))    #2
posts_ids = [345, 56, 34, 34]  
print(len(posts_ids))   #4
user_inputs = [True, '🤩', 'hi!', 10.5]  
print(len(user_inputs))  #4
```

Чтобы получить определённые значения, нужно использовать id

```python
inputs_ids = [True, '🤩', 'hi!', 10.5]  
print(inputs_ids[0])   #True
print(inputs_ids[1])   #🤩
print(inputs_ids[-1])   #10.5
```

Изменение значений 

```python
inputs_ids = [True, '🤩', 'hi!', 10.5]  
inputs_ids[0] = False  
inputs_ids[1] = '😋'  
print(inputs_ids)   #[False, '😋', 'hi!', 10.5] - перезаписали значения айдишника
```

Для удаление элемента, используется функция _del_ 

```python
inputs_ids = [True, '🤩', 'hi!', 10.5]  
del inputs_ids[0]  
print(len(inputs_ids))   #3
print(inputs_ids)   #['🤩', 'hi!', 10.5]
```

В списках могут встречаться словари, данный способ используется довольно часто

```python
users = [  
    {        
        'user_id': 123,  #ключ:значение
        'user_name': 'Anton'  #ключ:значение
    },  
    {  
        'user_id': 345,  #ключ:значение
        'user_name': 'Artur'  #ключ:значение
    }  
]  
  
print(len(users))  #2
print(users[1]['user_id'])   #345
```

Использование переменных

```python
my_fruit = 'Apple'  
other_fruit = 'Banana'  
new_fruit = 'lime'  
all_fruits = [my_fruit, other_fruit, new_fruit]  
print(all_fruits)   #['Apple', 'Banana', 'lime'] - сформированный список значений
```

Несуществующие элементы

```python
inputs_ids = [True, '🤩', 'hi!', 10.5]  
print(inputs_ids[10]) 

"""
Traceback (most recent call last):
  File "D:\Обучалка\Python\python\main.py", line 2, in <module>
    print(inputs_ids[10])
          ~~~~~~~~~~^^^^
IndexError: list index out of range

Ошибка при использовании несуществующего индекса
"""
```
### Методы списков

> Методы списков объектов наследуют от класса _LIST_

Некоторые методы
1. append - изменяет существующий список
2. pop - изменяет существующий список
3. remove
4. insert
5. sort
6. index
7. clear
8. copy
9. extend
10. reverse
11. count

_append_ - добавление новых элементов в конец списка

```python
happy_smiles = []  
happy_smiles.append('😄')  
happy_smiles.append('😁')  
happy_smiles.append('😂')  
happy_smiles.append('🙂')  
happy_smiles.append('😇')
print(len(happy_smiles))   #5
print(happy_smiles)   #['😄', '😁', '😂', '🙂', '😇']
```

_pop_ удаление из списка

```python
happy_smiles = ['😄', '😁', '😂', '🙂', '😇']  
happy_smiles.pop(4)  
print(happy_smiles) #['😄', '😁', '😂', '🙂']

#если указать пустой аргумент, то удаляет с конца списка

happy_smiles.pop()  
print(happy_smiles)  #['😄', '😁', '😂']

happy_smiles.pop()  
print(happy_smiles)  #['😄', '😁']

#Также можно узнать, какой элемент был удалён, присвоив список новой переменной и работать с удалённым элементом, который сохраняется в этой переменной

removed_element =  happy_smiles.pop()  
print(happy_smiles)   #['😄']
```


_sort_ - сортировка элементов

```python
posts_ids = [245, 45, 678, 234, 345]  
posts_ids.sort()  
print(posts_ids) #[45, 234, 245, 345, 678] - сортировка на увеличение

posts_ids.sort(reverse=True)  
print(posts_ids)   #[678, 345, 245, 234, 45] - сортировка по убыванию
```

### Разные операции со списками

#### Конвертация в список

```python
greeting = "Hello from Python"  
greeting_letters = list(greeting)  
print(greeting_letters)
# ['H', 'e', 'l', 'l', 'o', ' ', 'f', 'r', 'o', 'm', ' ', 'P', 'y', 't', 'h', 'o', 'n']

"""При конвертации словаря в список, значения ключей теряются"""
my_dict = {'a': 10, 'b': 20, 'c': 30}  
my_dict_keys = list(my_dict)  
print(my_dict_keys)
#['a', 'b', 'c']

```

#### Арифметические операции в списках

```python
ratings = [2.4, 5.0, 4.3, 3.7]  
print(min(ratings))  #2.4
print(max(ratings))  #5.0
print(sum(ratings))  #15.4
  
print(sum(ratings)/len(ratings))   #3.85
```

#### Объединение списков

```python
my_ratings = [2.5, 5.0]  
other_ratings = [2.6, 6.0, 4.0]  
all_ratings = my_ratings + other_ratings  
print(all_ratings)   #[2.5, 5.0, 2.6, 6.0, 4.0]

#отсортируем список
sorted_ratings = sorted(all_ratings)  
print(sorted_ratings)   #[2.5, 2.6, 4.0, 5.0, 6.0]
```

#### Нарезка списков

```python
ratings = [2.4, 5.0, 4.3, 3.7, 4.5]  
first_two_ratings = ratings[:2]  
print(first_two_ratings)  #[2.4, 5.0]
middle_ratings = ratings[1:-1]  
print(middle_ratings)    #[5.0, 4.3, 3.7]
last_two_ratings = ratings[-2:]  
print(last_two_ratings)   #[3.7, 4.5]
```


## Копирование списков

```python
my_cars = ['BMW', 'Mercedes']  
copied_cars = my_cars # копирование по ссылке  
copied_cars.append('Jeep')  
print(copied_cars)   #['BMW', 'Mercedes', 'Jeep']
print(id(my_cars) == id(copied_cars))   #True
#Такой метод не стоит использовать
```

> Вариант, которые используются

1 вариант

```python
my_cars = ['BMW', 'Mercedes']  
copied_cars = my_cars[:] # создание нового списка, используя slice
copied_cars.append('Jeep')  
print(copied_cars)   #['BMW', 'Mercedes', 'Jeep']
print(my_cars)   #['BMW', 'Mercedes']
print(id(my_cars) == id(copied_cars))  #False
#В данном случае переменная my_cars не изменена
```

2 вариант

```python
my_cars = ['BMW', 'Mercedes']  
copied_cars = my_cars.copy()   # создание нового списка использя метод copy 
copied_cars.append('Jeep')  
print(copied_cars)   #['BMW', 'Mercedes', 'Jeep']
print(my_cars)   #['BMW', 'Mercedes']
print(id(my_cars) == id(copied_cars))   #False
```

3 вариант

```python
my_cars = ['BMW', 'Mercedes']  
copied_cars = list(my_cars)  # создание нового списка в переменной, используя встроенную функцию list
copied_cars.append('Jeep')  
print(copied_cars)  #['BMW', 'Mercedes', 'Jeep']
print(my_cars)  #['BMW', 'Mercedes']
print(id(my_cars) == id(copied_cars))   #False
```

## Словари _dict_

> Словарь - набор элементов _ключ:значение_

> Порядок элементов в  _словаре_ <u>не имеет значения</u>

Сравнение словарей

```python
my_motorbike = {  
    'brand': 'Ducati',  
    'price': 150000,  
    'engine_vol': 1.2  
}  
  
other_motorbike = {  
    'brand': 'Ducati',  
    'engine_vol': 1.2,  
    'price': 150000  
}  
  
print(my_motorbike==other_motorbike)   #True

#Технически, для пайтон, это одинаковые словари и порядок ключей и значений не играет роль

print(id(my_motorbike)==id(other_motorbike))   #False
#Айди разные
```

### Изменение и удаление значений в словарях

#### Получение значений

```python
my_motorbike = {  
    'brand': 'Ducati',  
    'price': 150000,  
    'engine_vol': 1.2  
}  
  
print(my_motorbike['brand'])   #Ducati
print(my_motorbike['engine_vol'])   #1.2
```

#### Изменение значений

```python
my_motorbike = {  
    'brand': 'Ducati',  
    'price': 150000,  
    'engine_vol': 1.2  
}  
  
my_motorbike['engine_vol'] = 3  
print(my_motorbike)
#{'brand': 'Ducati', 'price': 150000, 'engine_vol': 3}
```

#### Добавление новых значений

```python
my_motorbike = {  
    'brand': 'Ducati',  
    'price': 150000,  
    'engine_vol': 1.2  
}  
  
my_motorbike['is_new'] = True  
print(my_motorbike)
#{'brand': 'Ducati', 'price': 150000, 'engine_vol': 1.2, 'is_new': True}
```

#### Удаление элементов

```python
my_motorbike = {  
    'brand': 'Ducati',  
    'price': 150000,  
    'engine_vol': 1.2  
}  
  
del my_motorbike['price']  
print(my_motorbike)
#{'brand': 'Ducati', 'engine_vol': 1.2}
```
