# infles67



Что такое символьная строка?

Символьная строка — это последовательность символов, относящихся к алфавиту определенного языка, которая может включать буквы, цифры, пробелы и специальные знаки. В программировании строки обычно представляются как массивы символов или специальными типами данных.

Почему неудобно заменять строки массивами символов?

Строки, представленные массивами символов, часто имеют фиксированную длину, что затрудняет управление ими (например, при добавлении или удалении символов). Также операции, такие как копирование, конкатенация или поиск подстроки, требуют ручного управления памятью и учета конца строки.

Как объявляются строки в школьном алгоритмическом языке и в Паскале?

В школьном алгоритмическом языке строки могут объявляться как переменные типа Строка, тогда как в Паскале строки могут объявляться с использованием типа String или фиксированного размера, например: Var myString: String[10];.

Как обращаться к элементу строки с заданным номером?

Для обращения к элементу строки по индексу используется синтаксис, например в Паскале: myString[i], где i — индекс (от 1 до длины строки).

Как вычисляется длина строки?

Длина строки вычисляется с использованием стандартной функции, например, в Паскале это функция Length(myString), которая возвращает количество символов в строке.

Что обозначает операция «+» применительно к строкам?

Операция «+» для строк обозначает конкатенацию, то есть объединение двух строк в одну. Например, str1 + str2 вернет строку, состоящую из символов, содержащихся в str1 и str2.

Перечислите основные операции со строками и соответствующие им стандартные функции.  

Конкатенация: + или Concat()

Длина: Length()

Поиск подстроки: Pos()

Извлечение подстроки: Copy()

Замена: StringReplace()

Преобразование регистра: UpCase(), LowerCase()

Как определить, что при поиске в строке образец не найден?

При поиске подстроки функция возвращает индекс первого вхождения. Если область поиска истощена и образец не найден, функция возвращает 0 или -1 (в зависимости от языка программирования).

Чем различаются средства школьного алгоритмического языка для работы со строками и Паскаля?

В школьном алгоритмическом языке функции и операции со строками, как правило, более ограничены и менее гибки, в то время как Паскаль предоставляет более широкий набор встроенных функций для работы со строками, позволяющих выполнять сложные операции более эффективно.

Как преобразовать число из символьного вида в числовой и обратно?

Для преобразования символьной строки в число можно использовать функции, такие как StrToInt() в Паскале, а для преобразования числа в строку используется IntToStr().

Почему строку не всегда можно преобразовать в число? Как определить, что преобразование закончилось неудачно?

Преобразование не удается, если строка содержит недопустимые символы (например, буквы). В Паскале можно использовать механизм обработки исключений или функции, которые возвращают статус преобразования.

Объясните выражение «рекурсивный перебор».

Рекурсивный перебор — это метод, при котором функция вызывает сама себя для решения задачи, разбивая её на более простые подзадачи до достижения базового случая.

Сравните на примерах рекурсивные и нерекурсивные методы решения переборных задач.

Пример рекурсивного метода: решение задачи о нахождении всех перестановок строки путем обмена текущего символа с каждым последующим. Нерекурсивный метод может использовать стек для хранения состояний и перебора всех вариантов, избегая самовызовов. Нерекурсивные методы иногда проще для понимания, но рекурсивные могут быть более лаконичными и выразительными.


0


















Давайте поочередно реализуем каждую из задач на Python.

### Задача 1: Замена букв и регистров

```python
def replace_letters_and_case(s):
    result = []
    for char in s:
        if char == 'а':
            result.append('б')
        elif char == 'б':
            result.append('а')
        elif char.isalpha():
            result.append(char.lower() if char.isupper() else char.upper())
        else:
            result.append(char)
    return ''.join(result)

input_string = input("Введите строку: ")
output_string = replace_letters_and_case(input_string)
print("Результат:", output_string)
```

### Задача 2: Проверка на палиндром

```python
def is_palindrome(s):
    s = ''.join(filter(str.isalnum, s)).lower()  # Убираем неалфавитные символы и переводим в нижний регистр
    return s == s[::-1]

input_string = input("Введите строку: ")
if is_palindrome(input_string):
    print("Строка является палиндромом.")
else:
    print("Строка не является палиндромом.")
```

### Задача 3: Разбор адреса файла на части

```python
def parse_file_path(file_path):
    parts = file_path.split('/')
    for part in parts:
        print(part)

input_file_path = input("Введите адрес файла: ")
parse_file_path(input_file_path)
```

### Задача 4: Вычисление суммы натуральных чисел

```python
def calculate_sum(expression):
    numbers = expression.split('+')
    return sum(int(num) for num in numbers)

input_expression = input("Введите сумму натуральных чисел (например '1+25+3'): ")
result = calculate_sum(input_expression)
print("Результат:", result)
```

### Задача 5: Вывод инициалов и фамилии

```python
def print_initials(full_name):
    parts = full_name.split()
    initials = ''.join(part[0] for part in parts[1:]) + '.'
    last_name = parts[0]
    return f"{initials} {last_name}"

input_full_name = input("Введите фамилию, имя и отчество: ")
result = print_initials(input_full_name)
print("Результат:", result)
```
Давайте поочередно реализуем предложенные задачи на Python.

### Задача 7: Рекурсивная версия процедуры `replaceAll`

```python
def replace_all_recursive(s, old, new):
    if old not in s:
        return s
    return replace_all_recursive(s.replace(old, new, 1), old, new)

def replace_all_iterative(s, old, new):
    while old in s:
        s = s.replace(old, new)
    return s

# Пример использования
input_string = input("Введите строку: ")
result_recursive = replace_all_recursive(input_string, 'а', 'б')
result_iterative = replace_all_iterative(input_string, 'а', 'б')

print("Рекурсивный результат:", result_recursive)
print("Итеративный результат:", result_iterative)
```

**Сравнение**: Рекурсивная версия более элегантна и проста в реализации, но может привести к переполнению стека для больших строк. Итеративная версия более устойчива и предпочтительнее для больших данных.

### Задача 8: Изменение расширения файла

```python
def change_extension(filename, new_extension):
    if '.' in filename:
        return '.'.join(filename.split('.')[:-1] + [new_extension])
    else:
        return filename + '.' + new_extension

input_filename = input("Введите имя файла: ")
new_extension = input("Введите новое расширение: ")
result_filename = change_extension(input_filename, new_extension)
print("Новое имя файла:", result_filename)
```

### Задача 9: Подсчет вхождений слова в строку

```python
def count_word_occurrences(s, word):
    return s.split().count(word)

input_string = input("Введите строку: ")
input_word = input("Введите слово для поиска: ")
count = count_word_occurrences(input_string, input_word)
print(f"Слово '{input_word}' встречается {count} раз(а).")
```

### Задача 10: Подсчет футболистов без голов, родившихся с 1998 по 2000

```python
def count_players_no_goals(players):
    count = 0
    for player in players:
        last_name, first_name, birth_year, goals = player.split()
        if 1998 <= int(birth_year) <= 2000 and int(goals) == 0:
            count += 1
    return count

N = int(input("Введите количество футболистов: "))
players_info = [input("Введите информацию о футболисте: ") for _ in range(N)]
result = count_players_no_goals(players_info)
print("Количество футболистов без голов, родившихся с 1998 по 2000:", result)
```

### Задача 11: Футболист с наибольшим количеством голов

```python
def player_with_most_goals(players):
    max_goals = -1
    best_player = ""
    for player in players:
        last_name, first_name, birth_year, goals = player.split()
        if int(goals) > max_goals:
            max_goals = int(goals)
            best_player = f"{last_name} {first_name}"
    return best_player, max_goals

best_player, goals = player_with_most_goals(players_info)
print(f"Футболист с наибольшим количеством голов: {best_player} ({goals} голов)")
```

### Задача 12: Футболисты, забившие хотя бы один гол

```python
def players_with_goals(players):
    return sorted([f"{player.split()[0]} {player.split()[1]}" for player in players if int(player.split()[-1]) > 0])

result_players = players_with_goals(players_info)
print("Футболисты, забившие хотя бы один гол:")
for player in result_players:
    print(player)
```

### Задача 13: Рекурсивный перебор слов заданной длины

```python
def generate_words(length, current_word='', alphabet='абв'):
    if length == 0:
        print(current_word)
        return
    for letter in alphabet:
        generate_words(length - 1, current_word + letter)

K = int(input("Введите длину слова: "))
generate_words(K)
```

### Задача 14: Слова из K букв с буквой «Ы» более 1 раза

```python
def generate_words_with_y(length, current_word=''):
    if length == 0:
        if current_word.count('Ы') > 1:
            print(current_word)
            return 1
        return 0
    count =
















Вот решения для задач, которые вы описали. Я предоставлю примеры кода на Python для каждой задачи.

### Задача 1: Нахождение минимальных и максимальных элементов матрицы и их индексов

```python
import numpy as np

# Генерация случайной матрицы
matrix = np.random.randint(0, 100, (5, 5))
print("Матрица:")
print(matrix)

min_value = np.min(matrix)
max_value = np.max(matrix)
min_index = np.argwhere(matrix == min_value)[0]
max_index = np.argwhere(matrix == max_value)[0]

print(f"Минимальный элемент: {min_value}, Индекс: {min_index}")
print(f"Максимальный элемент: {max_value}, Индекс: {max_index}")
```

### Задача 2: Нахождение минимальных и максимальных элементов с четными индексами

```python
import numpy as np

matrix = np.random.randint(0, 100, (5, 5))
print("Матрица:")
print(matrix)

even_elements = []
for i in range(matrix.shape[0]):
    for j in range(matrix.shape[1]):
        if i % 2 == 0 and j % 2 == 0:
            even_elements.append(matrix[i][j])

if even_elements:
    min_even = min(even_elements)
    max_even = max(even_elements)
    print(f"Минимальный элемент с четными индексами: {min_even}")
    print(f"Максимальный элемент с четными индексами: {max_even}")
else:
    print("Нет элементов с четными индексами.")
```

### Задача 3: Вывод строки матрицы

```python
import numpy as np

matrix = np.random.randint(0, 100, (5, 5))
print("Матрица:")
print(matrix)

row_index = 2  # Измените на нужный индекс
print(f"Строка с индексом {row_index}: {matrix[row_index]}")
```

### Задача 4: Вывод столбца матрицы

```python
import numpy as np

matrix = np.random.randint(0, 100, (5, 5))
print("Матрица:")
print(matrix)

col_index = 1  # Измените на нужный индекс
print(f"Столбец с индексом {col_index}: {matrix[:, col_index]}")
```

### Задача 5: Заполнение матрицы случайными числами выше главной диагонали

```python
import numpy as np

size = 5
matrix = np.zeros((size, size), dtype=int)
for i in range(size):
    for j in range(size):
        if j > i:
            matrix[i][j] = np.random.randint(1, 100)

print("Матрица с заполненными элементами выше главной диагонали:")
print(matrix)
```

### Задача 6: Заполнение матрицы случайными числами, нули выше побочной диагонали

```python
import numpy as np

size = 5
matrix = np.random.randint(0, 100, (size, size))
print("Исходная матрица:")
print(matrix)

for i in range(size):
    for j in range(size):
        if j < size - 1 - i:
            matrix[i][j] = 0

print("Матрица с нулями выше побочной диагонали:")
print(matrix)
```

### Задача 7: Заполнение матрицы 7x7 случайными числами

```python
import numpy as np

matrix = np.random.randint(0, 100, (7, 7))
print("Матрица 7x7:")
print(matrix)
```

### Задача 8: Заполнение матрицы по спирали и змейкой

```python
def spiral_fill(n, m):
    matrix = [[0]*m for _ in range(n)]
    num = 1
    left, right, top, bottom = 0, m-1, 0, n-1

    while left <= right and top <= bottom:
        for i in range(left, right + 1):
            matrix[top][i] = num
            num += 1
        top += 1

        for i in range(top, bottom + 1):
            matrix[i][right] = num
            num += 1
        right -= 1

        if top <= bottom:
            for i in range(right, left - 1, -1):
                matrix[bottom][i] = num
                num += 1
            bottom -=
































Вот решения для задач, которые вы описали. Я предоставлю примеры кода на Python для каждой задачи.

### Задача 9: Транспонирование квадратной матрицы

```python
import numpy as np

# Генерация случайной квадратной матрицы размером 4x4
size = 4
matrix = np.random.randint(0, 100, (size, size))
print("Исходная матрица:")
print(matrix)

# Транспонирование матрицы
transposed_matrix = matrix.T
print("Транспонированная матрица:")
print(transposed_matrix)
```

### Задача 10: Преобразование изображения в черно-белый

```python
import numpy as np

# Генерация случайной матрицы, представляющей изображение
rows, cols = 5, 5
image = np.random.randint(0, 256, (rows, cols))
print("Исходное изображение:")
print(image)

# Вычисление средней яркости
average_brightness = np.mean(image)
print(f"Средняя яркость: {average_brightness}")

# Преобразование изображения в черно-белый
bw_image = np.where(image < average_brightness, 0, 255)
print("Черно-белое изображение:")
print(bw_image)
```

### Задача 11: Отражение изображения сверху вниз

```python
import numpy as np

# Генерация случайной матрицы, представляющей изображение
image = np.random.randint(0, 256, (5, 5))
print("Исходное изображение:")
print(image)

# Отражение изображения сверху вниз
reflected_image = np.flipud(image)
print("Отраженное изображение:")
print(reflected_image)
```

### Задача 12: Поворот изображения вправо на 90 градусов

```python
import numpy as np

# Генерация случайной матрицы, представляющей изображение
image = np.random.randint(0, 256, (3, 3))
print("Исходное изображение:")
print(image)

# Поворот изображения вправо на 90 градусов
rotated_image = np.rot90(image, k=-1)  # k=-1 поворот вправо
print("Изображение после поворота вправо на 90 градусов:")
print(rotated_image)
```

### Задача 13: Игра в крестики-нолики

```python
def print_board(board):
    for row in board:
        print(" | ".join(row))
        print("-" * 9)

def check_winner(board):
    # Проверка строк
    for row in board:
        if row[0] == row[1] == row[2] != " ":
            return row[0]
    # Проверка столбцов
    for col in range(3):
        if board[0][col] == board[1][col] == board[2][col] != " ":
            return board[0][col]
    # Проверка диагоналей
    if board[0][0] == board[1][1] == board[2][2] != " ":
        return board[0][0]
    if board[0][2] == board[1][1] == board[2][0] != " ":
        return board[0][2]
    return None

def tic_tac_toe():
    board = [[" " for _ in range(3)] for _ in range(3)]
    current_player = "X"
    for _ in range(9):
        print_board(board)
        row = int(input(f"Игрок {current_player}, выберите строку (0-2): "))
        col = int(input(f"Игрок {current_player}, выберите столбец (0-2): "))
        
        if board[row][col] == " ":
            board[row][col] = current_player
            winner = check_winner(board)
            if winner:
                print_board(board)
                print(f"Игрок {winner} выиграл!")
                return
            current_player = "O" if current_player == "X" else "X"
        else:
            print("Эта ячейка уже занята. Попробуйте снова.")
    print_board(board)
    print("Ничья!")

tic_tac_toe()
```

### Задача 14: Подсчет островов на карте

```python
import numpy as np

def count_islands(map_matrix):
    rows, cols = map_matrix.shape
    visited = np.zeros((rows, cols), dtype=bool)

    def dfs(r,
