<div align="center">
  <h1> 30 Дней Python: День 24 - Статистика</h1>
  <a class="header-badge" target="_blank" href="https://www.linkedin.com/in/asabeneh/">
  <img src="https://img.shields.io/badge/style--5eba00.svg?label=LinkedIn&logo=linkedin&style=social">
  </a>
  <a class="header-badge" target="_blank" href="https://twitter.com/Asabeneh">
  <img alt="Twitter Follow" src="https://img.shields.io/twitter/follow/asabeneh?style=social">
  </a>

<sub>Автор:
<a href="https://www.linkedin.com/in/asabeneh/" target="_blank">Asabeneh Yetayeh</a><br>
<small>Второе издание: Июль, 2021</small>
</sub>
</div>

[<< День 23](../23_Day_Virtual_environment/23_virtual_environment.md) | [День 25 >>](../25_Day_Pandas/25_pandas.md)

![30DaysOfPython](../images/30daysofpython.png)

- [📘 День 24](#-день-24)
  - [Python для Статистического анализа](#python-для-статистического-анализа)
  - [Статистика](#статистика)
  - [Данные](#данные)
  - [Модуль Statistics](#модуль-statistics)
- [NumPy](#numpy)
  - [Импортирование NumPy](#импортирование-numpy)
  - [Создание массивов NumPy](#создание-массивов-numpy)
    - [Создание массивов целых чисел](#создание-массивов-целых-чисел)
    - [Создание массива с плавающей точкой](#создание-массива-с-плавающей-точкой)
    - [Создание массива логического типа данных](#создание-массива-логического-типа-данных)
    - [Создание многомерного массива](#создание-многомерного-массива)
    - [Преобразование массива Numpy в список](#преобразование-массива-numpy-в-список)
    - [Создание массива из кортежа](#создание-массива-из-кортежа)
    - [Форма (размерность) массива Numpy](#форма-размерность-массива-numpy)
    - [Тип данных массива Numpy](#тип-данных-массива-numpy)
    - [Размер (количество элементов) массива Numpy](#размер-количество-элементов-массива-numpy)
  - [Математические операции с использованием NumPy](#математические-операции-с-использованием-numpy)
    - [Сложение](#сложение)
    - [Вычитание](#вычитание)
    - [Умножение](#умножение)
    - [Деление](#деление)
    - [Остаток от деления](#остаток-от-деления)
    - [Целочисленное деление](#целочисленное-деление)
    - [Возведение в степень](#возведение-в-степень)
  - [Проверка типов данных](#проверка-типов-данных)
    - [Преобразование типов](#преобразование-типов)
  - [Многомерные массивы](#многомерные-массивы)
    - [Получение элементов из массива](#получение-элементов-из-массива)
  - [Срезы массива NumPy](#срезы-массива-numpy)
    - [Как перевернуть строки и весь массив?](#как-перевернуть-строки-и-весь-массив)
    - [Разворот строк и колонок массива](#разворот-строк-и-колонок-массива)
  - [Подставление значений в массивы](#подставление-значений-в-массивы)
      - [Генерация случайных чисел](#генерация-случайных-чисел)
    - [Генерация случайных чисел](#генерация-случайных-чисел-1)
  - [Numpy и Statistics](#numpy-и-statistics)
    - [Матрицы в numpy](#матрицы-в-numpy)
    - [Numpy numpy.arange()](#numpy-numpyarange)
      - [Что такое Arrange?](#что-такое-arrange)
    - [Создание последовательности чисел с использованием linspace](#создание-последовательности-чисел-с-использованием-linspace)
    - [Статистические функции NumPy с примерами](#статистические-функции-numpy-с-примерами)
    - [Как создать повторяющиеся последовательности?](#как-создать-повторяющиеся-последовательности)
    - [Как сгенерировать случайные числа?](#как-сгенерировать-случайные-числа)
    - [Линейная алгебра](#линейная-алгебра)
    - [Умножение матриц в NumPy с помощью np.matmul()](#умножение-матриц-в-numpy-с-помощью-npmatmul)
- [Резюме](#резюме)
  - [💻 Упражнение: День 24](#-упражнение-день-24)

# 📘 День 24

## Python для Статистического анализа

## Статистика

Статистика - это дисциплина, изучающая сбор, организацию, визуализацию, анализ, интерпретацию и представление данных.
Статистика является разделом математики, который рекомендуется изучать перед погружением в data science и машинное обучение. О статистике можно говорить часами, но в этом разделе мы сосредоточимся только на наиболее важной ее части.
После завершения этого урока вы сможете изучать веб-разработку, анализ данных, машинное обучение и data science. В любой из этих областей рано или поздно вам придется иметь дело с данными. Знания статистики, помогут вам делать правильные выводы. Как говорится "Данные говорят сами за себя".

## Данные

Что такое данные? Данные - это любой набор символов, который собирается и интерпретируется для определенных целей, обычно для анализа. Они могут представлять собой любые символы, включая текст и числа, изображения, звук или видео. Если данные не представлены в контексте, значит они не воспринимаются ни для человеком, ни для компьютером. Чтобы мы воспринимали и разбирались в данных, нам необходимо работать с ними с помощью различных инструментов.

Рабочий в анализе данных, data science или машинном обучении начинается с данных. Данные могут быть получены из источника данных или созданы. Существуют структурированные и неструктурированные данные.

## Модуль Statistics

Модуль statistics предоставляет функции для вычисления математической статистики числовых данных. Модуль не претендует на конкуренцию со сторонними библиотеками, такими как NumPy, SciPy или проприетарными полнофункциональными пакетами статистики, предназначенными для профессиональных статистиков, такими как Minitab, SAS и Matlab. Он ориентирован на уровень графических и научных калькуляторов.

# NumPy

В первом разделе мы определили Python как отличный язык программирования общего назначения, но с помощью других популярных библиотек, таких как NumPy, SciPy, Matplotlib, Pandas и др., он становится мощной средой для научных вычислений.

NumPy - это основная библиотека для научных вычислений в Python. Она предоставляет объект многомерного массива высокой производительности и инструменты для работы с массивами.

До сих пор мы использовали Visual Studio Code, но сейчас я рекомендую использовать Jupyter Notebook. Чтобы получить доступ к Jupyter Notebook, давайте установим [anaconda](https://www.anaconda.com/). Если вы будете использовать Anaconda, большинство распространенных пакетов будут уже установлены, и вам не нужно устанавливать их отдельно.

```sh
asabeneh@Asabeneh:~/Desktop/30DaysOfPython$ pip install numpy
```

## Импортирование NumPy

Jupyter Notebook доступен, если вы предпочитаете использоват [jupyter notebook](https://github.com/Asabeneh/data-science-for-everyone/blob/master/numpy/numpy.ipynb)

```py
    # Как импортировать NumPy
    import numpy as np
    # Как проверить версию пакета NumPy
    print('numpy:', np.__version__)
    # Проверка доступных методов
    print(dir(np))
```

## Создание массивов NumPy

### Создание массивов целых чисел

```py
    # Создание списка
    python_list = [1,2,3,4,5]

    # Проверка типа
    print('Type:', type (python_list)) # <class 'list'>
    #
    print(python_list) # [1, 2, 3, 4, 5]

    two_dimensional_list = [[0,1,2], [3,4,5], [6,7,8]]

    print(two_dimensional_list)  # [[0, 1, 2], [3, 4, 5], [6, 7, 8]]

    # Создание массива Numpy (Numerical Python) из списка.

    numpy_array_from_list = np.array(python_list)
    print(type (numpy_array_from_list))   # <class 'numpy.ndarray'>
    print(numpy_array_from_list) # массив([1, 2, 3, 4, 5])
```

### Создание массива с плавающей точкой

Создание массива Numpy с плавающей точкой из списка с параметром типа данных float.

```py
    # список
    python_list = [1,2,3,4,5]

    numy_array_from_list2 = np.array(python_list, dtype=float)
    print(numy_array_from_list2) # массив([1., 2., 3., 4., 5.])
```

### Создание массива логического типа данных

Создание массива логического типа данных из списка.

```py
    numpy_bool_array = np.array([0, 1, -1, 0, 0], dtype=bool)
    print(numpy_bool_array) # Иассив([False,  True,  True, False, False])
```

### Создание многомерного массива

Массив Numpy может иметь одну или несколько строк и столбцов.

```py
    two_dimensional_list = [[0,1,2], [3,4,5], [6,7,8]]
    numpy_two_dimensional_list = np.array(two_dimensional_list)
    print(type (numpy_two_dimensional_list))
    print(numpy_two_dimensional_list)
```

```sh
    <class 'numpy.ndarray'>
    [[0 1 2]
     [3 4 5]
     [6 7 8]]
```

### Преобразование массива Numpy в список

```python
# Мы можем преобразовать массив обратно в список с помощью функции tolist().
np_to_list = numpy_array_from_list.tolist()
print(type (np_to_list))
print('one dimensional array:', np_to_list)
print('two dimensional array: ', numpy_two_dimensional_list.tolist())
```

```sh
    <class 'list'>
    one dimensional array: [1, 2, 3, 4, 5]
    two dimensional array:  [[0, 1, 2], [3, 4, 5], [6, 7, 8]]
```

### Создание массива из кортежа

```py
# Массив Numpy из кортежа
# Создание кортежа
python_tuple = (1,2,3,4,5)
print(type (python_tuple)) # <class 'tuple'>
print('python_tuple: ', python_tuple) # python_tuple:  (1, 2, 3, 4, 5)

numpy_array_from_tuple = np.array(python_tuple)
print(type (numpy_array_from_tuple)) # <class 'numpy.ndarray'>
print('numpy_array_from_tuple: ', numpy_array_from_tuple) # numpy_array_from_tuple:  [1 2 3 4 5]
```

### Форма (размерность) массива Numpy

Метод shape возвращает форму (размерность) массива в виде кортежа. Первый элемент представляет количество строк, а второй элемент - количество столбцов. Если массив одномерный, то метод возвращает только колличество строк массива.

```py
    nums = np.array([1, 2, 3, 4, 5])
    print(nums)
    print('Форма массива nums:', nums.shape)
    print(numpy_two_dimensional_list)
    print('Форма массива numpy_two_dimensional_list:', numpy_two_dimensional_list.shape)
    three_by_four_array = np.array([[0, 1, 2, 3],
        [4,5,6,7],
        [8,9,10, 11]])
    print(three_by_four_array.shape)
```

```sh
    [1 2 3 4 5]
    Форма массива nums:  (5,)
    [[0 1 2]
     [3 4 5]
     [6 7 8]]
    Форма массива numpy_two_dimensional_list:  (3, 3)
    (3, 4)
```

### Тип данных массива Numpy

Типы данных включают: str (строка), int (целое число), float (число с плавающей точкой), complex (комплексное число), bool (логическое значение), list (список), None (пустое значение).

```py
int_lists = [-3, -2, -1, 0, 1, 2,3]
int_array = np.array(int_lists)
float_array = np.array(int_lists, dtype=float)

print(int_array)
print(int_array.dtype)
print(float_array)
print(float_array.dtype)
```

```sh
    [-3 -2 -1  0  1  2  3]
    int64
    [-3. -2. -1.  0.  1.  2.  3.]
    float64
```

### Размер (количество элементов) массива Numpy

В Numpy для получения количества элементов в массиве используется метод **size**.

```py
numpy_array_from_list = np.array([1, 2, 3, 4, 5])
two_dimensional_list = np.array([[0, 1, 2],
                              [3, 4, 5],
                              [6, 7, 8]])

print('Размер:', numpy_array_from_list.size) # 5
print('Размер:', two_dimensional_list.size)  # 3

```

```sh
    Размер: 5
    Размер: 9
```

## Математические операции с использованием NumPy

Массивы NumPy позволяют выполнять математические операции над элементами массива без явного использования циклов, в отличие от обычных списков Python. 
Ниже приведены основные математические операции, которые можно выполнять с помощью NumPy:

- Сложение (+)
- Вычитание (-)
- Умножение (\*)
- Деление (/)
- Остаток от деления (%)
- Целочисленное деление (//)
- Возведение в степень (\*\*)

### Сложение

```py
# Математические операции
# Сложение
numpy_array_from_list = np.array([1, 2, 3, 4, 5])
print('Исходный массив: ', numpy_array_from_list)
ten_plus_original = numpy_array_from_list  + 10
print(ten_plus_original)

```

```sh
    Исходный массив:  [1 2 3 4 5]
    [11 12 13 14 15]
```

### Вычитание

```python
# Вычитание
numpy_array_from_list = np.array([1, 2, 3, 4, 5])
print('Исходный массив: ', numpy_array_from_list)
ten_minus_original = numpy_array_from_list  - 10
print(ten_minus_original)
```

```sh
    Исходный массив:  [1 2 3 4 5]
    [-9 -8 -7 -6 -5]
```

### Умножение
```python
# Умножение
numpy_array_from_list = np.array([1, 2, 3, 4, 5])
print('Исходный массив: ', numpy_array_from_list)
ten_times_original = numpy_array_from_list * 10
print(ten_times_original)
```

```sh
    Исходный массив: [1 2 3 4 5]
    [10 20 30 40 50]
```

### Деление

```python
# Деление
numpy_array_from_list = np.array([1, 2, 3, 4, 5])
print('Исходный массив: ', numpy_array_from_list)
ten_times_original = numpy_array_from_list / 10
print(ten_times_original)
```

```sh
    Исходный массив: [1 2 3 4 5]
    [0.1 0.2 0.3 0.4 0.5]
```

### Остаток от деления

```python
# Остаток от деления
numpy_array_from_list = np.array([1, 2, 3, 4, 5])
print('Исходный массив: ', numpy_array_from_list)
ten_times_original = numpy_array_from_list % 3
print(ten_times_original)
```

```sh
    Исходный массив:  [1 2 3 4 5]
    [1 2 0 1 2]
```

### Целочисленное деление

```py
# Целочисленное деление
numpy_array_from_list = np.array([1, 2, 3, 4, 5])
print('Исходный массив: ', numpy_array_from_list)
ten_times_original = numpy_array_from_list // 10
print(ten_times_original)
```

### Возведение в степень 

```py
# Возведение в степень 
numpy_array_from_list = np.array([1, 2, 3, 4, 5])
print('Исходный массив: ', numpy_array_from_list)
ten_times_original = numpy_array_from_list  ** 2
print(ten_times_original)
```

```sh
    Исходный массив:  [1 2 3 4 5]
    [ 1  4  9 16 25]
```

## Проверка типов данных

```py
#Int,  Float числа
numpy_int_arr = np.array([1,2,3,4])
numpy_float_arr = np.array([1.1, 2.0,3.2])
numpy_bool_arr = np.array([-3, -2, 0, 1,2,3], dtype='bool')

print(numpy_int_arr.dtype)
print(numpy_float_arr.dtype)
print(numpy_bool_arr.dtype)
```

```sh
    int64
    float64
    bool
```

### Преобразование типов

Мы можем преобразовывать типы данных массивов NumPy.

1. Int во Float

```py
numpy_int_arr = np.array([1,2,3,4], dtype = 'float')
numpy_int_arr
```

    array([1., 2., 3., 4.])

2. Float в Int

```py
numpy_int_arr = np.array([1., 2., 3., 4.], dtype = 'int')
numpy_int_arr
```

```sh
    массив([1, 2, 3, 4])
```

3. Int в boolean

```py
np.array([-3, -2, 0, 1,2,3], dtype='bool')

```

```sh
    массив([ True,  True, False,  True,  True,  True])
```

4. Int в str

```py
numpy_float_list.astype('int').astype('str')
```

```sh
    массив(['1', '2', '3'], dtype='<U21')
```

## Многомерные массивы

```py
# 2-х мерный массив
two_dimension_array = np.array([(1,2,3),(4,5,6), (7,8,9)])
print(type (two_dimension_array))
print(two_dimension_array)
print('Форма: ', two_dimension_array.shape)
print('Размер:', two_dimension_array.size)
print('Тип данных:', two_dimension_array.dtype)
```

```sh
    <class 'numpy.ndarray'>
    [[1 2 3]
     [4 5 6]
     [7 8 9]]
    Форма:  (3, 3)
    Размер: 9
    Тип данных: int64
```

### Получение элементов из массива 

```py
# 2-х мерный массив
two_dimension_array = np.array([[1,2,3],[4,5,6], [7,8,9]])
first_row = two_dimension_array[0]
second_row = two_dimension_array[1]
third_row = two_dimension_array[2]
print('Первая строка: ', first_row)
print('Вторая строка:', second_row)
print('Третья строка: ', third_row)
```

```sh
    Первая строка: [1 2 3]
    Вторая строка: [4 5 6]
    Третья строка:  [7 8 9]
```

```py
first_column= two_dimension_array[:,0]
second_column = two_dimension_array[:,1]
third_column = two_dimension_array[:,2]
print('Первый столбец: ', first_column)
print('Второй столбец: ', second_column)
print('Третий столбец: ', third_column)
print(two_dimension_array)

```

```sh
    Первый столбец: [1 4 7]
    SВторой столбец: [2 5 8]
    Третий столбец: [3 6 9]
    [[1 2 3]
     [4 5 6]
     [7 8 9]]
```

## Срезы массива NumPy

Извлечение среза из массива NumPy осуществляется с использованием синтаксиса срезов, аналогичного срезам в списках Python.

```py
two_dimension_array = np.array([[1,2,3],[4,5,6], [7,8,9]])
first_two_rows_and_columns = two_dimension_array[0:2, 0:2]
print(first_two_rows_and_columns)
```

```sh
    [[1 2]
     [4 5]]
```

### Как перевернуть строки и весь массив?

```py
two_dimension_array[::]
```

```sh
    array([[1, 2, 3],
           [4, 5, 6],
           [7, 8, 9]])
```

### Разворот строк и колонок массива

```py
    two_dimension_array = np.array([[1,2,3],[4,5,6], [7,8,9]])
    two_dimension_array[::-1,::-1]
```

```sh
    array([[9, 8, 7],
           [6, 5, 4],
           [3, 2, 1]])
```

## Подставление значений в массивы

```python
    print(two_dimension_array)
    two_dimension_array[1,1] = 55
    two_dimension_array[1,2] =44
    print(two_dimension_array)
```

```sh
    [[1 2 3]
     [4 5 6]
     [7 8 9]]
    [[ 1  2  3]
     [ 4 55 44]
     [ 7  8  9]]
```

```py
    # Создание массива нулей
    # numpy.zeros(shape, dtype=float, order='C')
    numpy_zeroes = np.zeros((3,3),dtype=int,order='C')
    numpy_zeroes
```

```sh
    Массив([[0, 0, 0],
           [0, 0, 0],
           [0, 0, 0]])
```

```py
    # Создание массива единиц
    numpy_ones = np.ones((3,3),dtype=int,order='C')
    print(numpy_ones)
```

```sh
    [[1 1 1]
     [1 1 1]
     [1 1 1]]
```

```py
twoes = numpy_ones * 2
```

```py
    # Изменение формы массива
    # numpy.reshape(), numpy.flatten()
    first_shape  = np.array([(1,2,3), (4,5,6)])
    print(first_shape)
    reshaped = first_shape.reshape(3,2)
    print(reshaped)

```

```sh
    [[1 2 3]
     [4 5 6]]
    [[1 2]
     [3 4]
     [5 6]]
```

```py
flattened = reshaped.flatten()
flattened
```

```sh
    массив([1, 2, 3, 4, 5, 6])
```

```py
    ## Горизонтальное объединение
    np_list_one = np.array([1,2,3])
    np_list_two = np.array([4,5,6])

    print(np_list_one + np_list_two)

    print('Горизонтальное объединение: ', np.hstack((np_list_one, np_list_two)))
```

```sh
    [5 7 9]
    Горизонтальное объединение: [1 2 3 4 5 6]
```

```py
    ## Вертикальное объединение
    print('Вертикальное объединение:', np.vstack((np_list_one, np_list_two)))
```

```sh
    Вертикальное объединение: [[1 2 3]
     [4 5 6]]
```

#### Генерация случайных чисел

```py
    # Генерация случайного float числа
    random_float = np.random.random()
    random_float
```

```sh
    0.018929887384753874
```

```py
    # Генерация случайных float чисел
    random_floats = np.random.random(5)
    random_floats
```

```sh
    массив([0.26392192, 0.35842215, 0.87908478, 0.41902195, 0.78926418])
```

```py
    # Генерация случайных целых чисел от 0 до 10

    random_int = np.random.randint(0, 11)
    random_int
```

```sh
    4
```

```py
    # Генерация случайных целых чисел от 2 до 11 и создание одномерного массива
    random_int = np.random.randint(2,10, size=4)
    random_int
```

```sh
    массив([8, 8, 8, 2])
```

```py
    # Генерация случайных целых чисел от 2 до 10 и создание двумерного массива
    random_int = np.random.randint(2,10, size=(3,3))
    random_int
```

```sh
    массив([[3, 5, 3],
           [7, 3, 6],
           [2, 3, 3]])
```

### Генерация случайных чисел

```py
    # np.random.normal(mu, sigma, size)
    normal_array = np.random.normal(79, 15, 80)
    normal_array

```

```sh
    массив([ 89.49990595,  82.06056961, 107.21445842,  38.69307086,
            47.85259157,  93.07381061,  76.40724259,  78.55675184,
            72.17358173,  47.9888899 ,  65.10370622,  76.29696568,
            95.58234254,  68.14897213,  38.75862686, 122.5587927 ,
            67.0762565 ,  95.73990864,  81.97454563,  92.54264805,
            59.37035153,  77.76828101,  52.30752166,  64.43109931,
            62.63695351,  90.04616138,  75.70009094,  49.87586877,
            80.22002414,  68.56708848,  76.27791052,  67.24343975,
            81.86363935,  78.22703433, 102.85737041,  65.15700341,
            84.87033426,  76.7569997 ,  64.61321853,  67.37244562,
            74.4068773 ,  58.65119655,  71.66488727,  53.42458179,
            70.26872028,  60.96588544,  83.56129414,  72.14255326,
            81.00787609,  71.81264853,  72.64168853,  86.56608717,
            94.94667321,  82.32676973,  70.5165446 ,  85.43061003,
            72.45526212,  87.34681775,  87.69911217, 103.02831489,
            75.28598596,  67.17806893,  92.41274447, 101.06662611,
            87.70013935,  70.73980645,  46.40368207,  50.17947092,
            61.75618542,  90.26191397,  78.63968639,  70.84550744,
            88.91826581, 103.91474733,  66.3064638 ,  79.49726264,
            70.81087439,  83.90130623,  87.58555972,  59.95462521])
```

## Numpy и Statistics

```py
import matplotlib.pyplot as plt
import seaborn as sns
sns.set()
plt.hist(normal_array, color="grey", bins=50)
```

```sh
    (массив([2., 0., 0., 0., 1., 2., 2., 0., 2., 0., 0., 1., 2., 2., 1., 4., 3.,
            4., 2., 7., 2., 2., 5., 4., 2., 4., 3., 2., 1., 5., 3., 0., 3., 2.,
            1., 0., 0., 1., 3., 0., 1., 0., 0., 0., 0., 0., 0., 0., 0., 1.]),
     массив([ 38.69307086,  40.37038529,  42.04769973,  43.72501417,
             45.4023286 ,  47.07964304,  48.75695748,  50.43427191,
             52.11158635,  53.78890079,  55.46621523,  57.14352966,
             58.8208441 ,  60.49815854,  62.17547297,  63.85278741,
             65.53010185,  67.20741628,  68.88473072,  70.56204516,
             72.23935959,  73.91667403,  75.59398847,  77.27130291,
             78.94861734,  80.62593178,  82.30324622,  83.98056065,
             85.65787509,  87.33518953,  89.01250396,  90.6898184 ,
             92.36713284,  94.04444727,  95.72176171,  97.39907615,
             99.07639058, 100.75370502, 102.43101946, 104.1083339 ,
            105.78564833, 107.46296277, 109.14027721, 110.81759164,
            112.49490608, 114.17222052, 115.84953495, 117.52684939,
            119.20416383, 120.88147826, 122.5587927 ]),
     <a list of 50 Patch objects>)
```

### Матрицы в numpy

```py

four_by_four_matrix = np.matrix(np.ones((4,4), dtype=float))
```

```py
four_by_four_matrix
```

```sh
матрица([[1., 1., 1., 1.],
            [1., 1., 1., 1.],
            [1., 1., 1., 1.],
            [1., 1., 1., 1.]])
```

```py
np.asarray(four_by_four_matrix)[2] = 2
four_by_four_matrix
```

```sh

матрицы([[1., 1., 1., 1.],
            [1., 1., 1., 1.],
            [2., 2., 2., 2.],
            [1., 1., 1., 1.]])
```

### Numpy numpy.arange()

#### Что такое Arrange?

Иногда вам может потребоваться создать значения, равномерно распределенные в заданном интервале. Например, если вам нужно создать значения от 1 до 10, вы можете использовать функцию numpy.arange().

```py
# Создание списка с использованием range(starting, stop, step)
lst = range(0, 11, 2)
lst
```

```python
range(0, 11, 2)
```

```python
for l in lst:
    print(l)
```

```sh 0
    2
    4
    6
    8
    10
```

```py
# Аналогично range, функция arange numpy.arange(start, stop, step)
whole_numbers = np.arange(0, 20, 1)
whole_numbers
```

```sh
массив([ 0,  1,  2,  3,  4,  5,  6,  7,  8,  9, 10, 11, 12, 13, 14, 15, 16,
           17, 18, 19])
```

```py
natural_numbers = np.arange(1, 20, 1)
natural_numbers
```

```py
odd_numbers = np.arange(1, 20, 2)
odd_numbers
```

```sh
    массив([ 1,  3,  5,  7,  9, 11, 13, 15, 17, 19])
```

```py
even_numbers = np.arange(2, 20, 2)
even_numbers
```

```sh
    массив([ 2,  4,  6,  8, 10, 12, 14, 16, 18])
```

### Создание последовательности чисел с использованием linspace

```py
# numpy.linspace()
# numpy.logspace() in Python with Example
# Например, можно создать 10 значений от 1 до 5 с равными промежутками.
np.linspace(1.0, 5.0, num=10)
```

```sh
    array([1.        , 1.44444444, 1.88888889, 2.33333333, 2.77777778,
           3.22222222, 3.66666667, 4.11111111, 4.55555556, 5.        ])
```

```py
# исключение последнего значения в интервале
np.linspace(1.0, 5.0, num=5, endpoint=False)
```

```
массив([1. , 1.8, 2.6, 3.4, 4.2])
```

```py
# LogSpace
# LogSpace возвращает равномерно расположенные числа на логарифмической шкале. Logspace имеет те же параметры, что и np.linspace.

# Синтаксис:

# numpy.logspace(start, stop, num, endpoint)

np.logspace(2, 4.0, num=4)
```

```sh

массив([  100.        ,   464.15888336,  2154.43469003, 10000.        ])
```

```py
# для проверки размера массива
x = np.array([1,2,3], dtype=np.complex128)
```

```py
x
```

```sh
    массив([1.+0.j, 2.+0.j, 3.+0.j])
```

```py
x.itemsize
```

```sh
16
```

```py
# Индексация и спезы массивов NumPy
np_list = np.array([(1,2,3), (4,5,6)])
np_list

```

```sh
    массив([[1, 2, 3],
           [4, 5, 6]])
```

```py
print('Первая строка ', np_list[0])
print('Second row: ', np_list[1])

```

```sh

    Первая строка: [1 2 3]
    Первая строка: [4 5 6]
```

```p
    print('Первый столбец: ', np_list[:,0])
    print('Второй столбец: ', np_list[:,1])
    print('Третий столбец: ', np_list[:,2])

```

```sh
    Первый столбец:  [1 4]
    Второй столбец:  [2 5]
    Третий столбец:  [3 6]
```

### Статистические функции NumPy с примерами

NumPy предоставляет набор полезных статистических функций для нахождения минимума, максимума, среднего значения, медианы, процентиля, стандартного отклонения, дисперсии и т. д. из заданных элементов в массиве. Функции объявляются следующим образом:

- Функции NumPy
  - Минимум np.min()
  - Максимум np.max()
  - Среднее значение np.mean()
  - Медиана np.median()
  - Varience (дисперсия)
  - Percentile (процентиль)
  - Стандартное отклонение np.std()

```python
np_normal_dis = np.random.normal(5, 0.5, 100)
np_normal_dis
## min, max, mean, median, sd
print('min: ', two_dimension_array.min())
print('max: ', two_dimension_array.max())
print('mean: ',two_dimension_array.mean())
# print('median: ', two_dimension_array.median())
print('sd: ', two_dimension_array.std())
```

    min:  1
    max:  55
    mean:  14.777777777777779
    sd:  18.913709183069525

```python
min:  1
max:  55
mean:  14.777777777777779
sd:  18.913709183069525
```

```python
print(two_dimension_array)
print('Столбец с минимумом: ', np.amin(two_dimension_array,axis=0))
print('Столбец с максимумом: ', np.amax(two_dimension_array,axis=0))
print('=== Строка ==')
print('Строка с минимумом: ', np.amin(two_dimension_array,axis=1))
print('Строка с максимумом: ', np.amax(two_dimension_array,axis=1))
```

    [[ 1  2  3]
     [ 4 55 44]
     [ 7  8  9]]
    Cтолбец с минимумом: [1 2 3]
    Столбец с максимумом: [ 7 55 44]
    === Строка ==
    Строка с минимумом: [1 4 7]
    Строка с максимумом: [ 3 55  9]

### Как создать повторяющиеся последовательности?

```python
a = [1,2,3]

# Повторить всю последовательность 'a' дважды
print('Tile:   ', np.tile(a, 2))

# Повторить каждый элемент последовательности 'a' дважды
print('Repeat: ', np.repeat(a, 2))

```

    Tile:    [1 2 3 1 2 3]
    Repeat:  [1 1 2 2 3 3]

### Как сгенерировать случайные числа?

```python
# Одно случайное число в диапазоне [0,1)
one_random_num = np.random.random()
one_random_in = np.random
print(one_random_num)
```

    0.6149403282678213

```python
0.4763968133790438
```

    0.4763968133790438

```python
# Случайные числа в диапазоне [0,1) размером 2x3
r = np.random.random(size=[2,3])
print(r)
```

    [[0.13031737 0.4429537  0.1129527 ]
     [0.76811539 0.88256594 0.6754075 ]]

```python
# Случайный выбор из заданного набора значений
print(np.random.choice(['a', 'e', 'i', 'o', 'u'], size=10))
```

    ['u' 'o' 'o' 'i' 'e' 'e' 'u' 'o' 'u' 'a']

```python
['i' 'u' 'e' 'o' 'a' 'i' 'e' 'u' 'o' 'i']
```

    ['iueoaieuoi']

```python
# Случайные числа в диапазоне [0, 1] размером 2x2
rand = np.random.rand(2,2)
rand
```

    массив([[0.97992598, 0.79642484],
           [0.65263629, 0.55763145]])

```python
rand2 = np.random.randn(2,2)
rand2

```

    массив([[ 1.65593322, -0.52326621],
           [ 0.39071179, -2.03649407]])

```python
# Случайные целые числа в диапазоне [0, 10) размером 5x3
rand_int = np.random.randint(0, 10, size=[5,3])
rand_int
```

    массив([[0, 7, 5],
           [4, 1, 4],
           [3, 5, 3],
           [4, 3, 8],
           [4, 6, 7]])

```py
from scipy import stats
np_normal_dis = np.random.normal(5, 0.5, 1000) # среднее значение, стандартное отклонение, количество образцов
np_normal_dis
## min, max, mean, median, sd
print('Минимальное: ', np.min(np_normal_dis))
print('Максимальное: ', np.max(np_normal_dis))
print('Среднее: ', np.mean(np_normal_dis))
print('Медианное: ', np.median(np_normal_dis))
print('Мода: ', stats.mode(np_normal_dis))
print('Стандартное отклонение: ', np.std(np_normal_dis))
```

```sh

    Минимальное:  3.557811005458804
    mМаксимальноеax:  6.876317743643499
    Среднее:  5.035832048106663
    Медианное:  5.020161980441937
    Мода:  ModeResult(mode=array([3.55781101]), count=array([1]))
    Стандартное отклонение:  0.489682424165213

```

```python
plt.hist(np_normal_dis, color="grey", bins=21)
plt.show()
```

![png](../test_files/test_121_0.png)

```python
# numpy.dot(): Произведение матриц в Python с использованием NumPy
# Произведение матриц
# NumPy - мощная библиотека для вычислений с матрицами. Например, с помощью np.dot() можно вычислить произведение матриц.

# Синтаксис:

# numpy.dot(x, y, out=None)
```

### Линейная алгебра

1. Скалярное произведение

```python
## Линейная алгебра
### Скалярное произведение: произведение двух массивов
f = np.array([1,2,3])
g = np.array([4,5,3])
### 1*4+2*5 + 3*6
np.dot(f, g)  # 23
```

### Умножение матриц в NumPy с помощью np.matmul()

```python
### Matmul: произведение матриц
h = [[1,2],[3,4]]
i = [[5,6],[7,8]]
### 1*5+2*7 = 19
np.matmul(h, i)
```

```sh
    array([[19, 22],
           [43, 50]])

```

```py
## Определитель матрицы 2x2
### 5*8-7*6np.linalg.det(i)
```

```python
np.linalg.det(i)
```

    -1.999999999999999

```python
Z = np.zeros((8,8))
Z[1::2,::2] = 1
Z[::2,1::2] = 1
```

```python
Z
```

    array([[0., 1., 0., 1., 0., 1., 0., 1.],
           [1., 0., 1., 0., 1., 0., 1., 0.],
           [0., 1., 0., 1., 0., 1., 0., 1.],
           [1., 0., 1., 0., 1., 0., 1., 0.],
           [0., 1., 0., 1., 0., 1., 0., 1.],
           [1., 0., 1., 0., 1., 0., 1., 0.],
           [0., 1., 0., 1., 0., 1., 0., 1.],
           [1., 0., 1., 0., 1., 0., 1., 0.]])

```python
new_list = [ x + 2 for x in range(0, 11)]
```

```python
new_list
```

    [2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12]

```python
[2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12]
```

    [2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12]

```python
np_arr = np.array(range(0, 11))
np_arr + 2
```

массив([ 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12])

Мы используем линейное уравнение для величин, которые имеют линейную зависимость. Давайте рассмотрим пример ниже:

```python
temp = np.array([1,2,3,4,5])
pressure = temp * 2 + 5
pressure
```

array([ 7, 9, 11, 13, 15])

```python
plt.plot(temp,pressure)
plt.xlabel('Температура в oC')
plt.ylabel('Давление в атм')
plt.title('Температура vs Давление')
plt.xticks(np.arange(0, 6, step=0.5))
plt.show()
```

![png](../test_files/test_141_0.png)

Чтобы построить нормальное распределение Гаусса с использованием NumPy, как показано ниже, NumPy может генерировать случайные числа. Для создания случайной выборки нам понадобятся среднее (mu), стандартное отклонение (sigma) и количество точек данных.

```python
mu = 28
sigma = 15
samples = 100000

x = np.random.normal(mu, sigma, samples)
ax = sns.distplot(x);
ax.set(xlabel="x", ylabel='y')
plt.show()
```

![png](../test_files/test_143_0.png)

# Резюме

TВот основные различия между массивами NumPy и списками Python:

1. Массивы NumPy поддерживают векторизованные операции, в то время как списки этого не делают.
2. После создания массива нельзя изменить его размер. Вам придется создать новый массив или перезаписать существующий.
3. У каждого массива есть только один тип данных (dtype). Все элементы массива должны быть этого типа.
4. Эквивалентный массив NumPy занимает гораздо меньше места, чем список списков в Python.
5. Массивы NumPy поддерживают булево индексирование.

## 💻 Упражнение: День 24

1. Повторите все упражнения

🎉 Поздравляем! 🎉

[<< День 23](../23_Day_Virtual_environment/23_virtual_environment.md) | [День 25 >>](../25_Day_Pandas/25_pandas.md)
