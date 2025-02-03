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
temperature = float(str_temperature)  # конвертировали в десятичное число
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
  
print('Long string' > 'Long')  #True (выполняется посимвольное сравнение)

print('Long string' > 'Self')  #False (выполняется посимвольное сравнение)
  
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

### Использование переменных в словарях

#### Доступ к значению элемента с помощью переменной

```python
my_motorbike = {  
    'brand': 'Ducati',  
    'price': 150000,  
    'engine_vol': 1.2  
}  
key_name = 'brand'  
my_motorbike[key_name] = 'Mercedes'  
print(my_motorbike)
#{'brand': 'Mercedes', 'price': 150000, 'engine_vol': 1.2}
```

#### Вложенные словари

```python
my_motorbike = {  
    'brand': 'Ducati',  
    'engine_vol': 1.2,  
    'price_info':{  
        'price': 25000,  
        'is_available': True  
    }  
}  
print(my_motorbike['price_info']['price'])   #25000 
print(my_motorbike['price_info']['is_available'])   #True
```

#### Использование переменных для создания словарей

```python
brand = 'Ducati'  
bike_price = 25000  
engine_volume = 1.2  
  
my_motorbike = {  
    'brand' : brand,  
    'bike_price' : bike_price,  
    'engine_vol' : engine_volume,  
}  
  
print(my_motorbike)
#{'brand': 'Ducati', 'bike_price': 25000, 'engine_vol': 1.2}
```


### Длина словаря

```python
my_motorbike = {  
    'brand': 'Ducati',  
    'price': 150000,  
    'engine_vol': 1.2  
}  
print(len(my_motorbike))   #3
del my_motorbike['brand']  
print(my_motorbike)   #{'price': 150000, 'engine_vol': 1.2}
print(len(my_motorbike))   #2
```

### Несуществующие ключи и метод _get_

Чтобы проверить наличие ключа в словаре, пропишем синтаксис, который будет возвращать _None_

```python
my_motorbike = {  
    'brand': 'Ducati',  
    'price': 150000,  
    'engine_vol': 1.2  
}  
  
print(my_motorbike.get('model'))   #None
#Ошибки ключа нет
```

Также можно прописать значение, которое будет выведено при запросе вывода ключа

```python
my_motorbike = {  
    'brand': 'Ducati',  
    'price': 150000,  
    'engine_vol': 1.2  
}  
  
print(my_motorbike.get('qty', 0))   #0
                              ^
#значение на случай отсутствия ключа
```

> Метод _get_ стоит использовать, когда возникает неуверенность в наличии ключа

```python
my_motorbike = {  
    'brand': 'Ducati',  
    'price': 150000,  
    'engine_vol': 1.2  
}  
  
print(my_motorbike.get('engine_vol'))   #1.2
print(my_motorbike.get('brand'))   #Ducati
print(my_motorbike.get('qty', 0))   #0
```

Чтобы проверить значение атрибута словаря, нужно использовать <i>__doc__</i>

```python
my_motorbike = {}  
  
print(my_motorbike.__doc__)
#Получим документацию, как работать со словарём
"""
dict() -> new empty dictionary
dict(mapping) -> new dictionary initialized from a mapping object's
    (key, value) pairs
dict(iterable) -> new dictionary initialized as if via:
    d = {}
    for k, v in iterable:
        d[k] = v
dict(**kwargs) -> new dictionary initialized with the name=value pairs
    in the keyword argument list.  For example:  dict(one=1, two=2)
"""

"""
dict() -> новый пустой словарь
dict(сопоставление) -> новый словарь, инициализируемый из объекта сопоставления.
    пары (ключ, значение)
dict(повторяемый) -> новый словарь, инициализируемый как если бы через:
    d = {}
    для k, v в повторяющемся:
        d[k] = v
dict(**kwargs) -> новый словарь, инициализируемый парами имя=значение
    в списке аргументов ключевого слова.  Например: dict(one=1, two=2)
"""
```

Работа с методом <i>items</i>

```python
my_motorbike = {  
    'brand': 'Ducati',  
    'price': 150000,  
    'engine_vol': 1.2  
}  
  
print(my_motorbike.items())
#dict_items([('brand', 'Ducati'), ('price', 150000), ('engine_vol', 1.2)])
"""
В списке пары, в которых находятся ключ и значение - _кортеж_
Результат вывода является экземпляром класса dict_items
"""
```

Работа с методом <i>items</i>

```python
my_motorbike = {  
    'brand': 'Ducati',  
    'price': 150000,  
    'engine_vol': 1.2  
}  
print(my_motorbike.keys())
#dict_keys(['brand', 'price', 'engine_vol'])
```

### Копирование словаря copy()

```python
my_motorbike = {  
    'brand': 'Ducati',  
    'price': 150000,  
    'engine_vol': 1.2  
}  
new_motorbike = my_motorbike.copy()  
new_motorbike['type'] = 'ssd'  
print(new_motorbike)  
#{'brand': 'Ducati', 'price': 150000, 'engine_vol': 1.2, 'type': 'ssd'}
print(id(my_motorbike) == id(new_motorbike))   #False
```


### Конвертация других значений в словарь

```python
my_list = [['brand', 'BMW'], ['price', 30000]]  #список
  
my_dict = dict(my_list) #конвертация в словарь
print(my_dict)   # {'brand': 'BMW', 'price': 30000}
```

## Кортежи _tuple_

> Кортеж - упорядоченная последовательность элементов

_Кортеж изменять нельзя_

#### Структура и синтаксис

```python
my_fruits = ('apple', 'banana', 'orange')  
  
posts_id = (151, 565, 55, 88)  
  
user_inputs = (True, 'hi!', '😄', 10.6)   #в кортеже могут быть объекты _разных_ типов
```

> ПОРЯДОК В КОРТЕЖАХ ВАЖЕН

```python
my_fruits = ('apple', 'banana', 'orange')  
  
other_fruits = ('orange', 'banana', 'apple')  
  
print(my_fruits == other_fruits)   #False
```

#### Получение значений

```python
user_inputs = (True, 'hi!', '😄', 10.6)  
  
print(user_inputs[0])   #True
print(user_inputs[-1])  #10.6
```

> _Добавлять_ элементы нельзя
> _Удалять_ элементы нельзя

#### Кортеж словарей

```python
users = (  
    {        'username': 'artem',  
        'password': '<PASSWORD>',  
        'user_id': 345  
    },  
    {  
        'username': 'anton',  
        'password': '<PASSWORD>',  
        'user_id': 346  
    }  
)  
print(users[0]['user_id'])   #345
print(users[1]['username'])   #anton
  
users[0]['password'] = '<pass>'  
print(users[0]['password'])   #<pass>
print(users)
#({'username': 'artem', 'password': '<pass>', 'user_id': 345}, {'username': 'anton', 'password': '<PASSWORD>', 'user_id': 346})
```

> Объекты в кортеже, в данном случае словари, удалить нельзя!

#### Использование переменных

```python
my_fruits = 'apple'  
other_fruits = 'banana'  
new_fruita = 'lime'  
  
all_fruits = (my_fruits, other_fruits, new_fruita)  
print(all_fruits)   #('apple', 'banana', 'lime')
```

#### Объединение кортежей

```python
my_id = (456, 46, 789)  
  
other_id = (234, 56)  
  
all_id = my_id + other_id  
print(all_id)

#(456, 46, 789, 234, 56)
```

### Методы кортежей

1. count() - расчёт количества элементов кортежа
2. index() - вывод индекс определённого элемента

>Методы кортежей наследуется от класса tuple

```python
# count()
my_id = (456, 46, 789, 234, 56, 56)  
  
print(my_id.count(56))   #2

print(my_id.count(46))   #1
```

```python
# index()
my_id = (456, 46, 789, 234, 56, 56)  
  
print(my_id.index(56))   #1 если элемент встречается несколько раз, то возвращается индекс первого элемента
```

>Если нужно изменить кортеж, то конвертируем его в список, изменяем и конвертируем обратно в кортеж

```python
posts_id = (345, 567)  
  
posts_id_list = list(posts_id)  
posts_id_list.append(34)  
print(type(posts_id_list))   #<class 'list'>
print(posts_id_list)   #[345, 567, 34]
  
posts_id_tuple = tuple(posts_id_list)  
print(type(posts_id_tuple))   #<class 'tuple'>
print(posts_id_tuple)   #(345, 567, 34)
```

Существует способ узнать индексы повторяющихся элементов в кортеже

```python
posts_id = (345, 567, 5, 56, 5, 5)  
  
index_one = posts_id.index(5)  
print(index_one)  
index_two = posts_id.index(5, index_one + 1)  
print(index_two)  
index_three = posts_id.index(5, index_two + 1)  
print(index_three)
```

Методу _index_, можно передавать как 1 аргумент, так и 2, указывая во втором аргументе некий счётчик, который указывает с какой позиции провести вычисление

## Наборы _set()_

> _Набор_ - неупорядоченная последовательность элементов
> _Набор_ содержит только <u>уникальные</u> элементы
> Изменять наборы можно
> В _наборах_ обычно сохраняют однотипные объекты

```python
my_fruits = {'apple', 'banana', 'orange'}
print(my_fruits) 
#{'orange', 'apple', 'banana'}
print(type(my_fruits))   #<class 'set'>

posts_ids = {151, 565, 55, 88}  
  
user_inputs = {True, 'hi!', '😄', 10.6}
```

 Индексов у элементов нет

```python
my_fruits = {'apple', 'banana', 'orange'}  
print(my_fruits[2])

#TypeError: 'set' object is not subscriptable

#Преобразуем набор в список
fruits_list = list(my_fruits)

#Теперь можем использовать магический метод _getitem_
print(fruits_list.__getitem__(0))   #apple

#Это равносильная выводу результата записи
print(fruits_list[0])   #apple
```

#### Изменяемые объекты в наборах

```python
lists_set = {[1, 2], [20, 4]}  
  
print(lists_set)

""" в наборы нельзя добавлять изменяемые объекты
Traceback (most recent call last):
  File "D:\Обучалка\Python\python\main.py", line 1, in <module>
    lists_set = {[1, 2], [20, 4]}
                ^^^^^^^^^^^^^^^^^
TypeError: unhashable type: 'list'
"""
```

> Удалять с помощью _del_ нельзя

```python
posts_ids = {3, 5, 7, 98, 0}  
del posts_ids[2]

"""
Traceback (most recent call last):
  File "D:\Обучалка\Python\python\main.py", line 2, in <module>
    del posts_ids[2]
        ~~~~~~~~~^^^
TypeError: 'set' object doesn't support item deletion
"""
```


```python
my_set = {(10, 10), 3, 5, 86}  
print(my_set)

#{(10, 10), 3, 5, 86}
# При добавлении в набор неизменяемых объектов, в данном случае кортеж, ошибок не возникает
```

Для создания или вызова пустого набора, нужно прописать 

```python
my_set = set()  
print(my_set)  #set()
print(type(my_set))  #<class 'set'> (набор)
```


### Методы наборов

>['add', 'clear', 'copy', 'difference', 'difference_update', 'discard', 'intersection', 'intersection_update', 'isdisjoint', 'issubset', 'issuperset', 'pop', 'remove', 'symmetric_difference', 'symmetric_difference_update', 'union', 'update']

Метод **_add()_** - добавление одного элемента в набор

```python
photo_sizes = {'1500*156', '800*600'}  
  
photo_sizes.add('1500*200')  
print(photo_sizes)  #{'1500*156', '800*600', '1500*200'}
```

Метод **_union()_** - объединение наборов - |

```python
photo_sizes = {'1500*1080', '800*600'}  
other_sizes = {'1500*200', '800*600'}
  
all_sizes = photo_sizes.union(other_sizes)  
  
print(all_sizes)
#{'1500*200', '1500*1080', '800*600'}
# Есл встречаются одинаковые значения в обоих множествах, то останется 1 экземпляр элемента
```

Метод _**intersection()**_ - метод поиска элементов в пересечении, иными словами дублёра - &

```python
photo_sizes = {'1500*1080', '800*600'}  
other_sizes = {'1500*200', '800*600'}  
  
commons_photo = photo_sizes.intersection(other_sizes) 

print(commons_photo)  #{'800*600'}

#можно использовать оператор &
photo_sizes = {'1500*1080', '800*600'}  
other_sizes = {'1500*200', '800*600'}  
  
print(photo_sizes & other_sizes) #{'800*600'}
```

Метод _**issubset()**_ - позволяет проверить находится ли каждый элемент множества `set` в последовательности `other`. Метод возвращает `True`, если множество `set` **является подмножеством** итерируемого объекта `other`, если нет, то вернет `False`.

```python
nums = {10, 5, 35}  
other_nums = {20, 5, 12, 10, 35}  
  
res = nums.issubset(other_nums)  
print(res)   #True

#Метод показал, что множество nums, является подмножеством other_nums
```

Метод _***issuperset**_ - **в Python** **используется для определения, содержит ли набор все элементы другого набора**. ( - )

```python
nums = {10, 5, 35}  
other_nums = {20, 5, 12, 10, 35}  
  
res = other_nums.issuperset(nums)  
print(res)   #True

#Если прописать иначе
res = nums.issuperset(other_nums)
print(res)  #False

#Множество other_nums не является подмножеством nums
```

Метод _**discard**_ - **удаляет указанный элемент из набора**, если он присутствует.

```python
other_nums = {20, 5, 12, 10, 35}  
  
  
print(other_nums.discard(20))  #None - результат срабатывания метода
print(other_nums)  # {35, 5, 10, 12} - набор изменён
```

Метод _**remove**_ - метод также удаляет переданный в аргумент объект, но если его нет в наборе, выведет ошибку

```python
other_nums = {20, 5, 12, 10, 35}  
  
other_nums.remove(20)  
  
print(other_nums)  #{35, 5, 10, 12}
```

Метод _**copy()**_ метод копирования объекта

```python
other_nums = {20, 5, 12, 10, 35}  
  
copied = other_nums.copy()  
  
print(copied)  #{35, 20, 5, 10, 12}
```

### Симметричная разница в наборах

Метод _**symmetric_difference**_ - **возвращает все элементы, присутствующие в заданных наборах, за исключением элементов в их пересечениях**. [1](https://tr-page.yandex.ru/translate?lang=en-ru&url=https%3A%2F%2Fwww.programiz.com%2Fpython-programming%2Fmethods%2Fset%2Fsymmetric_difference)

```python
other_nums = {20, 5, 12, 10, 35}  
  
copied = other_nums.copy()  
other_nums.add(50)  
copied.add(9)  
print(other_nums)  #{50, 35, 20, 5, 10, 12}
print(copied)  #{35, 20, 5, 9, 10, 12}
print(other_nums.symmetric_difference(copied))  #{50, 9} - это элементы, которые есть в одном множестве, но нет в другом (объединение минус пересечение)


## Диапазоны _**range()**_

> **Диапазон** - упорядоченная неизменяемая последовательность элементов
>**Диапазоны** обычно используются в циклах

```python
range = range(10)  
print(range)  # range(0, 10)
print(type(range))  # <class 'range'>
print(list(range))  # [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
```

10 - является верхней границей, которая не включается в диапазон выводы

>**Существует три формы вызова range**: 

1. **range(stop)** — создаёт последовательность чисел от 0 до stop (не включая stop). 
2. **range(start, stop)** — создаёт последовательность чисел от start до stop (не включая stop).
3. **range(start, stop, step)** — создаёт последовательность чисел от start до stop (не включая stop) с шагом step. 

**Параметры функции**:

- **start** — начальное значение последовательности (по умолчанию 0). 
- **stop** — конечное значение последовательности (не включается).
- **step** — шаг последовательности (по умолчанию 1). 

Иной способ задания с шагом

```python
range = range(10, 20, 2)
  
print(range)  #range(10, 20, 2)
  
print(list(range))  #[10, 12, 14, 16, 18]
#где 3 - шаг диапазона
```

>Индексы элементов в диапазоне

```python
range = range(10, 20, 2)  
  
print(range[0])  10
print(range[1])  12
print(range[2])  14
print(range[3])  16
print(range[4])  18
print(range[5])  

"""Traceback (most recent call last):
  File "D:\Обучалка\Python\python\main.py", line 8, in <module>
    print(range[5])
          ~~~~~^^^
IndexError: range object index out of range
"""
```

>Итерация в диапазоне

>_**Итерация**_ - повторение какого-либо действия или процесса. В широком смысле итерацией можно назвать любой циклический процесс, при котором действия повторяются снова и снова.

```python
range = range(10, 20, 3)  

for i in range:  
    print(i)
#либо
for i in range(10,20,3):  
    print(i)
#10
#13
#16
#19
```

Методы диапазона

>['count', 'index']

_**start**_ - старт диапазона
_**stop**_ - конец диапазона
_**step**_ - шаг диапазона
_**index**_ - индекс

```python
range = range(10)  
  
print(range.start, range.stop)  #0 10
```

_**count**_ - вывод 0 или 1, аналогия болевого значения

```python
range = range(10)  
  
print(range.count(9))  #1 - такой элемент в диапазоне есть
```

>Задача - создать список с интервалом и шагом, итерировать по нему и записать значения в элемент списка

>Решение
```python
my_list = []  
for i in range(1, 11, 2):  
    my_list.append(i)  
    print(my_list)
```

### Последовательности: сравнение типов

| Тип              | Изменения | Порядок | Одинаковые элементы |
| :--------------- | --------- | ------- | ------------------: |
| list (список)    | ✔️        | ✔️      |                  ✔️ |
| tuple (кортеж)   | ❌         | ✔️      |                  ✔️ |
| set (набор)      | ✔️        | ❌       |                   ❌ |
| range (диапазон) | ❌         | ✔️      |                   ❌ |
| dict (словарь)   | ✔️        | ❌       |                   ❌ |
| str (строка)     | ❌         | ✔️      |                  ✔️ |


## Функция zip

**Функция zip в Python** **объединяет элементы нескольких итерируемых объектов (кортежей, списков, строк) в пары**. Она возвращает итератор, где каждый кортеж состоит из элементов, взятых по одному из каждого исходного объекта. 

**Синтаксис функции**: 

zip(*итерируемые объекты)

. Она может принимать любое количество аргументов — итерируемых объектов. 


**Некоторые задачи, которые решает функция zip**:

- **Создание словарей**, где ключи и значения берутся из итерируемых объектов. Например, если есть перечисление двух параметров, её удобно применять для составления словаря, где первое значение будет ключом, а второе — значением.
- **Объединение информации из разных источников**, например, из файлов или баз данных. Можно объединить сведения о клиентах, заказах, товарах, чтобы получить полную информацию о каждой транзакции.
- **Итерация по нескольким объектам одновременно** при помощи цикла for. Это особенно полезно, когда нужно обрабатывать сведения из разных источников сразу.
- **Оптимизация кода**, чтобы сделать его более читаемым, особенно когда работает несколько объектов. Вместо вложенных циклов for можно использовать функцию для объединения данных и обработки их в одной итерации.

Функция поддерживает разные параметры, такие как strict и longest, которые позволяют управлять поведением функции при работе с объектами разной длины.

```python
fruits = ["apple", "banana", "cherry"]  
quantities = [12, 24, 344]  
fruits_qtys_zip = zip(fruits, quantities)  
print(fruits_qtys_zip)  #<zip object at 0x00000250ACDCDD40>
fruits_qtys_list = list(fruits_qtys_zip)  
print(fruits_qtys_list)  
#[('apple', 12), ('banana', 24), ('cherry', 344)] - список
```

Также итерируемый объект, можно выводить с помощью цикла

```python
fruits = ['apple', 'banana', 'cherry']  
quantities = [12, 24, 344]  
fruits_qtys_zip = zip(fruits, quantities)  
for fruit, quantity in fruits_qtys_zip:  
    print(fruit, quantity)

#apple 12
#banana 24
#cherry 344

#Можно изменить вывод результата
for item in fruits_qtys_zip:  
    print(item)

#('apple', 12)
#('banana', 24)
#('cherry', 344)
```

#### Конвертация zip в dict

```python
fruits = ['apple', 'banana', 'cherry']  
quantities = [12, 24, 344]  
fruits_qtys_zip = zip(fruits, quantities)  
fruits_qtys_dict = dict(fruits_qtys_zip)  
print("Словарь:", fruits_qtys_dict)

#Словарь: {'apple': 12, 'banana': 24, 'cherry': 344}
```

> При конвертации _zip_ объекта в _словарь_ допускается только 2 аргумента в вызове функции _zip_

> Задача
- Создать в списка, в одном из них будет товар, во втором будут цены  объединить и создать список, потом словарь

#### Создание списка
```python
product = ['tomato', 'orange', 'banana', 'apple']  
price = [34, 67, 78]  
  
zip_convert = zip(product, price)  
print(zip_convert)  #<zip object at 0x000001ABC9E7A800>
print(list(zip_convert))   #[('tomato', 34), ('orange', 67), ('banana', 78)]
```

#### Создание словаря

```python
product = ['tomato', 'orange', 'banana', 'apple']  
price = [34, 67, 78]  
zip_convert = zip(product, price)  
print(dict(zip_convert))

#{'tomato': 34, 'orange': 67, 'banana': 78}
```
## Изменение объектов в Python

Переменная содержит ссылку на объект и с помощью id можно узнать ячейку

Переменные могут ссылаться на один объект в памяти

> Адреса неизменяемых объектов

```python
my_number = 10  
print(id(my_number))  #140727532192968
  
other_number = 10  
print(id(other_number))  #140727532192968
  
print(id(10))  #140727532192968
```

В данном примере обращение к постоянному неизменяемому значение в ячейке памяти

```python
first_num = 10  
second_num = first_num  
  
print(id(first_num), id(second_num))  

#140727532192968 140727532192968

second_num += 4  # создание нового объекта
print(id(first_num), id(second_num))

#140727532192968 140727532193096
```

#### Поведение изменяемых объектов

##### Пример 1 - список

```python
my_list = [1,2,3,4,5]
print(id(my_list))  #2661862713088
  
other_list = [1,2,3,4,5]
print(id(other_list))  #2661862563968
  
print(id([1,2,3,4,5]))  #2661862521728
```

##### Пример 2 - словарь

```python
info = {  
    'name': 'Artem',  
    'age': 28,  
}  
info_copy = info  
print(id(info_copy))  #2161184138176
print(id(info), info)  
# 2161184138176 {'name': 'Artem', 'age': 28}

"""Копируем только ссылку"""
```

Добавим новый ключ с новым значением

```python
info = {  
    'name': 'Artem',  
    'age': 28,  
}  
info_copy = info  
info['reviews_qty'] = 5  
print(id(info_copy))  #1766475752384
print(id(info), info)  #1766475752384 {'name': 'Artem', 'age': 28, 'reviews_qty': 5}

"""Созданы новые ячейки в памяти"""
```

##### Пример 3 - словарь

```python
my_info = {  
    'name': 'Artem',  
    'age': 28,  
}  
other_info = {  
    'name': 'Anton',  
    'age': 22,  
}  
print(id(my_info), id(other_info))  #1520810255296 1520810651968
```

Добавим ключ во второй словарь
```python
my_info = {  
    'name': 'Artem',  
    'age': 28,  
}  
other_info = {  
    'name': 'Anton',  
    'age': 22,  
}  
other_info['rating'] = 4.0  
print(id(my_info), id(other_info))  #2510134764480 2510135161152

"""Адреса изменились"""
```

#### Изменения копий

> Как избежать изменения копий

Пример 1

```python
my_info = {  
    'name': 'Artem',  
    'age': 28,  
}  
other_info = my_info.copy()  
other_info['rating'] = 4.0  
print(my_info)  #{'name': 'Artem', 'age': 28, 'reviews': ['Great course!']}
print(other_info)  #{'name': 'Artem', 'age': 28, 'reviews': ['Great course!']}

"""За счёт копирования таким способом, остаются ссылки, ибо копирование поверхностное"""
```

Для полного копирования объекта нужно использовать функцию _**deepcopy()**_ импортируя модуль _**copy**_

```python
from copy import deepcopy 
  
my_info = {  
    'name': 'Artem',  
    'age': 28,  
    'reviews': []  
}  
info_copy = deepcopy(my_info)
info_copy['reviews'].append('Great course!')  
print(my_info)  #{'name': 'Artem', 'age': 28, 'reviews': []}
print(info_copy)  #{'name': 'Artem', 'age': 28, 'reviews': ['Great course!']}
```
## Функции

> _**Функция**_ - блок кода, который можно выполнять многократно

```python
def sum(a, b):  # функция с именем
    c = a + b  # тело функции
    print(c)  


a = 5  
b = 6  
sum(a, b)  # вызов функции

#11

a = 9  
b = 6  
sum(a, b)

#15



"""Функция используется многократно, для вывода разных результатов"""
```

> _**Функция**_ это объект, как всё в Python - <class 'function'>

> Функция возвращает _**None**_, если нет ключевого слова _**return**_

```python
def sum(a, b):  
    c = a + b  
  
print(sum(3, 4))  # None

def sum(a, b):  
    c = a + b  
    return c  
  
print(sum(3, 4))  # 7
```

#### Функция _**pass**_

Функция `pass` в Python используется в качестве заполнителя, когда нужно написать код позже или просто требуется выполнить синтаксическую структуру языка (например, создать тело класса, функции или цикла), но не добавлять никакого конкретного действия.

Это может быть полезно для:

- Создания скелета программы перед добавлением функциональности.
- Формирования шаблонов для будущих функций или классов.
- Указания на то, что блок кода должен быть написан в будущем.

Использование `pass` позволяет избежать ошибок и предупреждений от интерпретатора Python, связанных с отсутствием кода там, где он ожидается.

## Передача неизменяемых объектов в функцию

В Python передача неизменяемых объектов (таких как строки, числа и кортежи) в функции происходит по значению. Это означает, что при передаче объекта в функцию создаётся копия значения аргумента, которая затем используется внутри функции.

При изменении такого объекта внутри функции изменения не будут отражены за пределами функции, так как была создана новая копия. Однако если функция возвращает изменённый объект, то эти изменения будут видны снаружи.

Пример:

```python
def my_function(my_string):
    my_string = my_string + " World!"
    return my_string

my_greeting = "Hello"
modified_greeting = my_function(my_greeting)
print("Inside function:", modified_greeting)  # Prints "Hello World!"
print("Outside function:", my_greeting)     # Prints "Hello"
```

В этом примере строка «Hello» передаётся в функцию `my_function`, где она изменяется. Но поскольку строка является неизменяемым объектом, изменение копии внутри функции не влияет на оригинал. Чтобы увидеть изменения, нужно присвоить результат функции другой переменной.


## Передача изменяемых объектов в функцию

```python
def increase_person_age(person):  
    person['age'] += 1  
    return person  


person_one ={  
    'name': 'Bob',  
    'age': 21,  
}  
  
increase_person_age(person_one)  
print(person_one['age'])  #22
```

В данном примере функция `increase_person_age` принимает один аргумент — словарь `person`, который является изменяемым объектом. Внутри функции значение ключа `'age'` увеличивается на 1 с помощью операции `+=`. Затем функция возвращает изменённый словарь.

В основной части кода создаётся словарь `person_one` с данными о человеке. Затем вызывается функция `increase_person_age`, передавая ей словарь `person_one`. После вызова функции печатается значение ключа `'age'`, которое теперь равно 22.

Таким образом, изменения, сделанные внутри функции, отражаются в исходном словаре, поскольку он был передан по ссылке. Это особенность работы с изменяемыми объектами в Python.

> Внутри функции _**не рекомендуется**_ изменять _**внешние_** объекты

#### Как избежать изменения внешних объектов в функции

```python
def increase_person_age(person):  
    person_copy = person.copy()  #создаём копию внутри функции задавая новую переменную, тем самым не затрагивая внешние ссылки
    person_copy['age'] += 1  
    return person_copy  
  
  
person_one = {  
    'name': 'Bob',  
    'age': 21,  
}  
  
new_person = increase_person_age(person_one)  
print(new_person['age'])  #22
print(person_one['age'])  #21
```

Чтобы избежать изменения внешних объектов в функции в Python, можно использовать несколько подходов:

1. **Копирование объекта.** Создайте копию переданного объекта внутри функции с помощью методов копирования или срезов. Это позволит вам работать с копией объекта, не затрагивая оригинальный объект.
    
2. **Использование неизменяемых типов данных.** Если возможно, используйте неизменяемые типы данных, такие как строки, числа и кортежи. Они не могут быть изменены после создания, что предотвращает случайное изменение внешних объектов.
    
3. **Возврат нового объекта.** Вместо изменения переданного объекта создайте новый объект внутри функции и верните его. Таким образом, вы сможете контролировать, какие изменения будут внесены во внешний мир.
    
4. **Передача копии объекта.** При вызове функции передайте копию объекта, используя методы копирования или срезы. Это гарантирует, что функция будет работать только с копией, а не с исходным объектом.
    
5. **Использование аргументов только для чтения.** В некоторых случаях можно использовать аргументы только для чтения, чтобы предотвратить их изменение внутри функции. Однако это может привести к ошибкам, если функция попытается изменить объект, который был передан как аргумент только для чтения.
    
6. **Применение функций высшего порядка.** Используйте функции высшего порядка, которые принимают другие функции в качестве аргументов и возвращают новые функции. Это позволяет контролировать доступ к внешним объектам и предотвращать их случайное изменение.
    
7. **Использование контекстных менеджеров.** Контекстные менеджеры предоставляют возможность управлять ресурсами и объектами, гарантируя их безопасное использование и освобождение. Они могут помочь предотвратить случайное изменение объектов внутри функции.
    
8. **Возвращение изменённого объекта.** Верните изменённый объект из функции, но сохраните исходный объект без изменений. Это даст возможность контролировать процесс внесения изменений и при необходимости откатиться к первоначальному состоянию.
    

Выбор подхода зависит от конкретной ситуации и требований  проекта.

> Задача
- Создайте функцию merge_lists_to_dict
- У функции должно быть два параметра
- Функция должна объединить два списка, используя встроенную функцию zip
- Конвертируйте объект zip в словарь и верните его из функции
- Вызовите функцию, передав ей два списка в качестве аргументов
- Выведите результат вызова функции в терминал

>Решение

```python
def  merge_lists_to_dict(a, b):  
    create_zip_list = zip(a, b)  # <zip object at 0x000002BC6A8FC4C0>
    create_dict_list = dict(create_zip_list)  
    return create_dict_list
  
  
list1 = [1, 2, 3]  
list2 = [4, 5, 6]  
  
result = merge_lists_to_dict(list1, list2)  
print(result)  #{1: 4, 2: 5, 3: 6}
```

### Аргументы с ключевыми словами

```python
def get_posts_info(name, posts_qty):  
    info = f"{name} wrote {posts_qty} posts"    
    return info  
  
  
info = get_posts_info(name='Artem', posts_qty=29)  
print(info)  # Artem wrote 29 posts

""" 
В данном примере аргументы с ключевыми словами внесены в функцию, поэтому порядок аргументов не важен
"""
```

> Использование аргументов с ключевыми словами делает код более _**читабельным

### Объединение именованных аргументов в словарь

```python
def get_posts_info(**person):  
    print(person)  # {'name': 'Artem', 'posts_qty': 29}
    info = f"{person['name']} wrote {person['posts_qty']} posts"    
    return info  
  
  
info = get_posts_info(name='Artem', posts_qty=29)  
print(info)  # Artem wrote 29 posts
```

Функция **get_posts_info** принимает один аргумент — словарь с данными о пользователе (аргумент person). В этом словаре есть два ключа: name и posts_qty.

Функция выводит на экран содержимое словаря и формирует строку с информацией о пользователе, используя ключи name и posts_qty из словаря. Затем функция возвращает эту строку.

В основной части кода мы вызываем функцию get_posts_info и передаём ей словарь с ключами name и posts_qty, где name имеет значение 'Artem', а posts_qty — значение 29. Результат вызова функции сохраняется в переменной info.

Таким образом, функция get_posts_info позволяет получить информацию о пользователе в виде строки.
