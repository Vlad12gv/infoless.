1. Что такое цикл?  
Цикл — это конструкция программирования, позволяющая повторять выполнение определенного блока кода несколько раз в зависимости от заданного условия или переменной.

2. Сравните цикл с переменной и цикл с условием.  
- Цикл с переменной: выполняется заданное число раз, обычно с помощью счетчика. Преимущества — простота, удобство при известном количестве итераций. Недостатки — не всегда подходит, когда количество итераций заранее неизвестно.
- Цикл с условием: выполняется до тех пор, пока выполняется условие. Преимущества — гибкость в случае неизвестного количества итераций. Недостатки — может привести к бесконечному циклу, если условие не изменяется.

3. Что означает выражение «цикл с предусловием»?  
Цикл с предусловием — это цикл, который сначала проверяет условие. Если условие истинно, выполняется тело цикла. В противном случае цикл не выполняется ни разу.

4. В каком случае цикл с предусловием не выполняется ни разу?  
Цикл с предусловием не выполняется ни разу, если изначально условие ложно.

5. В каком случае программа, содержащая цикл с условием, может зациклиться?  
Программа может зациклиться, если условие окончания цикла никогда не становится истинным. Например:
i := 0;
while (i < 10) do begin
  // Код без изменения значения i
end;


6. В каком случае цикл с переменной не выполняется ни разу?  
Цикл с переменной не выполняется ни разу, если переменная начального значения нарушает условия выполнения цикла. Например, если цикл начинается с i=10 и проверка i < 5.

7. Верно ли, что любой цикл с переменной можно заменить циклом с условием?  
Да, любой цикл с переменной можно заменить циклом с условием. Но обратное утверждение неверно: не любой цикл с условием можно заменить на цикл с переменной, так как у цикла с переменной фиксированное количество итераций, а у цикла с условием — нет.

8. В каком случае можно заменить цикл с условием на цикл с переменной?  
Если известно количество итераций заранее, например, в случае суммирования первых N чисел.

9. Как будет работать программа, которая считает количество цифр введённого числа, при вводе отрицательного числа?  
Если программа ожидает положительное число, то при вводе отрицательного числа может работать неправильно или выдавать неверный результат. Нужно добавить обработку отрицательных чисел, например, преобразовать число в положительное.

---

Задания:

1. Программа для нахождения произведения без операции умножения:
a = int(input("Введите первое число: "))
b = int(input("Введите второе число: "))
product = 0
for _ in range(abs(b)):
    product += abs(a)
if (a < 0) != (b < 0):
    product = -product
print("Произведение:", product)


2. Программа для нахождения суммы от 1 до N с двумя типами циклов:
Цикл с условием:
N = int(input("Введите натуральное число N: "))
sum_ = 0
i = 1
while i <= N:
    sum_ += i
    i += 1
print("Сумма от 1 до N (циклом с условием):", sum_)

Цикл с переменной:
N = int(input("Введите натуральное число N: "))
sum_ = 0
for i in range(1, N + 1):
    sum_ += i
print("Сумма от 1 до N (циклом с переменной):", sum_)


3. Программа для вывода первых N четных натуральных чисел:
N = int(input("Введите натуральное число N: "))
for i in range(1, N + 1):
    if i % 2 == 0:
        print(i)


4. Программа для вывода квадратов чисел в диапазоне:
a = int(input("Введите первое натуральное число: "))
b = int(input("Введите второе натуральное число: "))
for i in range(a, b + 1):
    print(f"{i}*{i}={i*i}")


5. Программа для вывода суммы квадратов чисел в диапазоне:
a = int(input("Введите первое натуральное число: "))
b = int(input("Введите второе натуральное число: "))
sum_of_squares = 0
for i in range(a, b + 1):
    sum_of_squares += i * i
print("Сумма квадратов:", sum_of_squares)


6. Программа для вывода N псевдослучайных чисел:
import random
N = int(input("Введите количество случайных чисел: "))
for _ in range(N):
    print(random.randint(1, 100))

7. Поиск пятизначных чисел с данными условиями:
for number in range(10000, 100000):
    if number % 133 == 125 and number % 134 == 111:
        print(number)


8. Программа для вывода натуральных чисел, делящихся на каждую из своих цифр:
N = int(input("Введите натуральное число N: "))
for number in range(1, N + 1):
    digits = [int(d) for d in str(number) if int(d) != 0]  # убираем нули
    if all(number % d == 0 for d in digits):
        print(number)


9. Поиск чисел Армстронга:
for num in range(100, 10000):
    digits = [int(d) for d in str(num)]
    power = len(digits)
    if sum(d ** power for d in digits) == num:
        print(num)


10. Программа для вывода автоморфных чисел, не превосходящих M:

M = int(input("Введите натуральное число M: "))
for num in range(M + 1):
    if str(num ** 2).endswith(str(num)):
        print(num)


---

11. Программа, которая считает количество чётных цифр введённого числа:

number = input("Введите число: ")
count_even = sum(1 for digit in number if int(digit) % 2 == 0)
print("Количество чётных цифр:", count_even)


---

12. Программа, которая считает сумму цифр введённого числа:

number = input("Введите число: ")
digit_sum = sum(int(digit) for digit in number)
print("Сумма цифр:", digit_sum)


---

13. Программа, которая определяет, содержит ли введённое число две одинаковые цифры, стоящие рядом:

number = input("Введите число: ")
has_adjacent_duplicate = any(number[i] == number[i + 1] for i in range(len(number) - 1))
print("Содержит ли число две одинаковые цифры рядом:", has_adjacent_duplicate)


---

14. Программа, которая определяет, состоит ли введённое число из одинаковых цифр:

number = input("Введите число: ")
is_all_same = all(digit == number[0] for digit in number)
print("Состоит ли число из одинаковых цифр:", is_all_same)


---

15. Программа, которая определяет, содержит ли введённое число по крайней мере две одинаковые цифры (не обязательно рядом):

number = input("Введите число: ")
has_duplicate = len(set(number)) < len(number)
print("Содержит ли число хотя бы две одинаковые цифры:", has_duplicate)


---

16. Программа для вывода четных степеней числа 2 от \(2^{10}\) до \(2^{2}\) в порядке убывания:

Используя цикл с условием:

exponent = 10
while exponent >= 2:
    if exponent % 2 == 0:
        print(f"2^{exponent} = {2 ** exponent}")
    exponent -= 1


Используя цикл с переменной:

for exponent in range(10, 1, -1):
    if exponent % 2 == 0:
        print(f"2^{exponent} = {2 ** exponent}")


---

17. Программа, реализующая алгоритм Евклида для нахождения НОД:

a = int(input("Введите первое число: "))
b = int(input("Введите второе число: "))
steps = 0

while b != 0:
    a, b = b, a - b
    steps += 1

print("НОД =", a)
print("Количество шагов:", steps)


---

18. Программа с модифицированным алгоритмом Евклида:

a = int(input("Введите первое число: "))
b = int(input("Введите второе число: "))
steps = 0

while b != 0:
    a, b = b, a % b
    steps += 1

print("НОД =", a)
print("Количество шагов:", steps)


---

19. Таблица для двух версий алгоритма Евклида:

# Для целей демонстрации, значения a и b могут быть переданы заранее
a = 64168
b = 82678

# Выполнение для первого метода
steps1 = 0
while b != 0:
    a, b = b, a - b
    steps1 += 1

nod1 = a

# Выполнение для второго метода
a = 64168
b = 82678
steps2 = 0
while b != 0:
    a, b = b, a % b
    steps2 += 1

nod2 = a

print("НОД(a, b):", nod1)
print("Шаги-1:", steps1)
print("Шаги-2:", steps2)


---

20. Программа, которая вводит 10 чисел и вычисляет их сумму и произведение:

sum_nums = 0
product = 1

for _ in range(10):
    number = int(input("Введите число: "))
    sum_nums += number
    product *= number

print("Сумма:", sum_nums)
print("Произведение:", product)


---

21. Программа, которая вводит числа до тех пор, пока не будет введено число 0:

sum_nums = 0
product = 1
while True:
    number = int(input("Введите число (0 для выхода): "))
    if number == 0:
        break
    sum_nums += number
    product *= number

print("Сумма:", sum_nums)
print("Произведение:", product)


---

22. Программа, которая вводит числа до тех пор, пока не будет введено число 0:

min_num = float('inf')
max_num = float('-inf')

while True:
    number = int(input("Введите число (0 для выхода): "))
    if number == 0:
        break
    if number < min_num:
        min_num = number
    if number > max_num:
        max_num = number

print("Минимальное число:", min_num)

print("Максимальное число:", max_num)


---

23. Программа, вычисляющая факториал натурального числа:

import math

N = int(input("Введите натуральное число: "))
factorial = 1
for i in range(1, N + 1):
    factorial *= i

print("Факториал:", factorial)


Для больших значений N, например, 20, возможен очень большой результат (20! = 2432902008176640000), который может не помещаться в стандартные типы данных, однако в Python поддерживаются большие целые числа.

---

24. Программа для вычисления A:

a = int(input("Введите натуральное число a: "))
N = int(input("Введите натуральное число N: "))
A = a ** N  # это выражение может быть изменено, в зависимости от конкретного требования
print("A =", A)


---

25. Программа, которая выводит на экран все цифры числа:

number = input("Введите число: ")
for digit in number:
    print(digit)


---

26. Программа, выводящая первые N чисел Фибоначчи:

N = int(input("Введите натуральное число N: "))
fib = [1, 1]
while len(fib) < N:
    fib.append(fib[-1] + fib[-2])
print(f"Первые {N} чисел Фибоначчи: {fib[:N]}")


---

27. Программа, выводящая все простые числа в диапазоне от a до b:

a = int(input("Введите число a: "))
b = int(input("Введите число b: "))

def is_prime(n):
    if n < 2:
        return False
    for i in range(2, int(n**0.5) + 1):
        if n % i == 0:
            return False
    return True

primes = [num for num in range(a, b + 1) if is_prime(num)]
print("Простые числа в диапазоне:", primes)


---

28. Программа, определяющая, является ли число N совершенным:

N = int(input("Введите натуральное число N: "))
sum_divisors = sum(i for i in range(1, N) if N % i == 0)
is_perfect = sum_divisors == N
print("Является ли N совершенным:", is_perfect)


---

29. Программа, находящая совершенные числа в диапазоне от 1 до N:

N = int(input("Введите натуральное число N: "))

def is_perfect(num):
    return sum(i for i in range(1, num) if num % i == 0) == num

perfect_numbers = [num for num in range(1, N + 1) if is_perfect(num)]
print("Совершенные числа в диапазоне:", perfect_numbers)

---

30. Программа для продажи мастики в ящиках по 15, 17 и 21 кг с целью получить ровно 185 кг:

Для решения этой задачи нам нужно найти неотрицательные целые решения уравнения:

[ 15x + 17y + 21z = 185 \]

где \( x \), \( y \) и \( z \) - количество ящиков по 15, 17 и 21 кг соответственно. Мы можем использовать итерации для проверки всех возможных комбинаций. Вот программа:

count = 0

for x in range(186 // 15 + 1):  # Ящики по 15 кг
    for y in range(186 // 17 + 1):  # Ящики по 17 кг
        for z in range(186 // 21 + 1):  # Ящики по 21 кг
            if 15 * x + 17 * y + 21 * z == 185:
                print(f"15*{x} + 17*{y} + 21*{z}")
                count += 1

print("Количество способов:", count)


---

31. Программа для нахождения значения дроби 1/N и выделения периода дроби:

Чтобы вывести дробь в формате \( 1/N \) и определить период, нам нужно использовать деление с остатком. Вот программа, которая это делает:

def find_period(n):
    result = "0."
    seen_remainders = {}
    numerator = 1
    index = 0

    while True:
        numerator *= 10
        digit = numerator // n
        remainder = numerator % n

        result += str(digit)

        if remainder == 0:
            return result  # если деление закончилось, возвращаем результат

        if remainder in seen_remainders:
            period_start = seen_remainders[remainder]
            non_period = result[:period_start]
            period = result[period_start:]

            return f"{non_period}({period})"

        seen_remainders[remainder] = len(result)  # фиксируем место начала текущего остатка
        numerator = remainder

N = int(input("Введите натуральное число N: "))
print("1/", N, "=", find_period(N), sep="")


---

32. Моделирование телевикторины для 1000 раундов:

В этой задаче мы будем моделировать выбор участника и выбор ведущего, а затем сравнивать стратегии (оставить тот же ящик или выбрать другой). Вот программа:

import random

def simulate_monty_hall(rounds=1000):
    stay_wins = 0
    switch_wins = 0

    for _ in range(rounds):
        # Случайно выбираем ящик с призом
        prize_box = random.randint(0, 2)
        # Участник случайно выбирает один из трех ящиков
        player_choice = random.randint(0, 2)
        
        # Ведущий открывает пустой ящик, который не выбран участником и не содержит приз (только если есть возможность)
        empty_box = next(box for box in range(3) if box != player_choice and box != prize_box)
        
        # Участник меняет выбор на оставшийся ящик
        new_choice = next(box for box in range(3) if box != player_choice and box != empty_box)

        # Проверяем, выиграл ли участник, оставаясь или меняя выбор
        if player_choice == prize_box:
            stay_wins += 1
        if new_choice == prize_box:
            switch_wins += 1

    print("Количество побед, оставаясь при своём выборе:", stay_wins)
    print("Количество побед, меняя выбор:", switch_wins)

simulate_monty_hall()

*Вопросы и задания*

1. *Что такое процедуры? В чём смысл их использования?*
   Процедуры — это именованные фрагменты кода, которые выполняют определённую задачу. Они позволяют структурировать программу, повторно использовать код и улучшать его читаемость.

2. *Как оформляются процедуры в школьном алгоритмическом языке и в Паскале?*
   В школьном алгоритмическом языке процедуры могут оформляться как "Процедура имя(параметры) ... КонецПроцедуры". В Паскале они оформляются аналогично с ключевым словом "procedure":

   pascal
   procedure MyProcedure(parameter: type);
   begin
       // тело процедуры
   end;
   

3. *Достаточно ли включить процедуру в текст программы, чтобы она «сработала»?*
   Нет, нужно также вызвать процедуру в тексте основной программы. В противном случае код процедуры не выполнится.

4. *Что такое параметры? Зачем они используются?*
   Параметры — это значения, которые передаются в процедуру. Они позволяют обрабатывать входные данные и делать процедуру более универсальной.

5. *Какие переменные называются локальными? Где они объявляются?*
   Локальные переменные объявляются внутри процедуры и доступны только в пределах этой процедуры.

6. *Как оформляются процедуры, имеющие несколько параметров?*
   Процедуры с несколькими параметрами оформляются, перечисляя параметры через запятую в заголовке процедуры:

   pascal
   procedure MyProcedure(param1: type1; param2: type2);
   

7. *Что такое изменяемые параметры? Зачем они используются?*
   Изменяемые параметры позволяют процедуре изменять значения переменных, переданных ей в качестве аргументов. Это полезно, когда нужно возвращать несколько значений из процедуры.

8. *Как в заголовке процедуры отличить изменяемый параметр от неизменяемого? Приведите примеры.*
   В Питоне все параметры неизменяемые по умолчанию, кроме объектов. В Паскале изменяемые параметры обозначаются ключевым словом "var":

   pascal
   procedure MyProcedure(var param: type);
   

9. *Какие типы параметров выделяются в школьном алгоритмическом языке? Как они объявляются?*
   В школьном алгоритмическом языке можно выделить простые, массивные и структурные параметры. Они объявляются через соответствующий тип данных.

---

*Подготовьте сообщение*

а) *Процедуры в языке Си*
   
   В языке Си процедуры называются функциями. Они имеют заголовок, который включает имя функции, тип возвращаемого значения и параметры. Например:

   c
   void myFunction(int param) {
       // тело функции
   }
   

б) *Процедуры в языке Python*
   
   В Python процедуры представляют собой функции, которые определяются с помощью ключевого слова def. Пример:

   python
   def my_function(param):
       # тело функции
   

---

*Задачи*

1. *Процедура для вывода числа в восьмеричной системе:*
   pascal
   procedure PrintOctalNumber(num: Integer);
   begin
       if num < 810 then
           WriteLn(Octal(num));
   end;
   

2. *Процедура для вывода числа в шестнадцатеричной системе:*
   pascal
   procedure PrintHexadecimalNumber(num: Integer);
   begin
       if num < 65536 then
           WriteLn(Hex(num));
   end;
   

3. *Процедура для вывода квадрата из звёздочек:*
   pascal
   procedure PrintStarSquare(N: Integer);
   var
       i, j: Integer;
   begin
       for i := 1 to N do
       begin
           for j := 1 to N do
               Write('*');
           WriteLn;
       end;
   end;
   

4. *Процедура для вывода возраста с правильными окончаниями:*
   pascal
   procedure PrintAge(age: Integer);
   begin
       if (age mod 10 = 1) and (age mod 100 <> 11) then
           WriteLn(age, ' год')
       else if (age mod 10 >= 2) and (age mod 10 <= 4) and (age mod 100 <> 12) and (age mod 100 <> 13) and (age mod 100 <> 14) then
           WriteLn(age, ' года')
       else
           WriteLn(age, ' лет');
   end;
   

5. *Процедура для вывода числа прописью:*
   ```pascal
   procedure PrintNumberInWords(num: Integer);
   begin
   // Реализация вывода числа прописью
   end;
   

6. **Процедура для вывода первых N чисел Фибоначчи:**
   pascal
   procedure PrintFibonacci(N: Integer);
   var
       a, b, temp, i: Integer;
   begin
       a := 0;
       b := 1;
       for i := 1 to N do
       begin
           Write(a, ' ');
           temp := a;
           a := b;
           b := temp + b;
       end;
   end;
   

7. **Процедура для проверки простоты числа:**
   pascal
   procedure CheckPrime(var num: Integer; var isPrime: Boolean);
   var
       i: Integer;
   begin
       isPrime := True;
       if num < 2 then isPrime := False;
       for i := 2 to Trunc(Sqrt(num)) do
           if (num mod i = 0) then
           begin
               isPrime := False;
               Break;
           end;
   end;
   

8. **Процедура для вывода цифр числа, начиная с последней:**
   pascal
   procedure PrintDigitsReversed(num: Integer);
   begin
       while num > 0 do
       begin
           WriteLn(num mod 10);
           num := num div 10;
       end;
   end;
   

9. **Процедура для вывода цифр числа, начиная с первой:**
   pascal
   procedure PrintDigitsForward(num: Integer);
   var
       digits: array of Integer;
       i: Integer;
   begin
       while num > 0 do
       begin
           SetLength(digits, Length(digits) + 1);
           digits[High(digits)] := num mod 10;
           num := num div 10;
       end;
       for i := High(digits) downto 0 do
           WriteLn(digits[i]);
   end;
   

10. **Процедура для вывода делителей числа:**
    pascal
    procedure PrintDivisors(num: Integer);
    var
        i: Integer;
    begin
        for i := 1 to num do
            if (num mod i = 0) then
                Write(i, ' ');
        WriteLn;
    end;
    

11. **Процедура для вывода линии из символов:**
    pascal
    procedure PrintLine(M: Integer);
    var
        i: Integer;
    begin
        for i := 1 to M do
            Write('-');
        WriteLn;
    end;
    

12. **Процедура для вывода числа в римской системе счисления:**
    pascal
    procedure PrintRoman(num: Integer);
    var
        roman: array[1..13] of String = ('I', 'II', 'III', 'IV', 'V', 'VI', 
                                           'VII', 'VIII', 'IX', 'X', 'L', 'C', 'D', 'M');
    begin
        // Реализация для преобразования числа в римские цифры
    end;



    # par60-61

    1. Что такое функция? Чем она отличается от процедуры?
   Функция — это блок кода, который принимает входные параметры, выполняет определенные операции и возвращает значение. Процедура, в отличие от функции, не возвращает значения, а просто выполняет действия. Основное различие состоит в том, что функции возвращают результат, а процедуры — нет.

2. Как оформляются функции в тексте программы (сравните школьный алгоритмический язык и Паскаль)?
   В школьном алгоритмическом языке функции часто оформляются просто с указанием их названия и входных параметров, без строгого определения типов. Например:
      Функция Максимум(а, b)
       Если а > b тогда
           Вернуть а
       Иначе
           Вернуть b
   КонецФункции
   
   В Паскале функции имеют строгую структуру с указанием типа возвращаемого значения и определением типов параметров:
      function Максимум(a, b: Integer): Integer;
   begin
       if a > b then
           Максимум := a
       else
           Максимум := b;
   end;
   

3. Как по тексту программы определить, какое значение возвращает функция? Приведите пример.
   Чтобы определить значение, возвращаемое функцией, следует изучить ее тело и выйти на оператор, который возвращает соответствующее значение. Например:
      function Сумма(a, b: Integer): Integer;
   begin
       Сумма := a + b;
   end;
   
   В данном случае функция Сумма возвращает сумму двух целых чисел.

4. Какие функции называются логическими? Зачем они нужны?
   Логические функции — это функции, которые возвращают булевы значения (истина или ложь). Они часто используются для проверок и условий, например, для определения, является ли число простым, или для работы с условиями в логических выражениях.

### Сообщения

а) Функции в языке Си
   Функции в языке Си определяются с указанием типа возвращаемого значения, имени функции и параметров. Синтаксис выглядит следующим образом:
      return_type function_name(parameter_list) {
       // тело функции
   }
   
   Пример функции, вычисляющей сумму двух чисел:
      int sum(int a, int b) {
       return a + b;
   }
   

б) Функции в языке Python
   В Python функции определяются с использованием ключевого слова def и не требуют указания типов параметров. Пример функции, вычисляющей произведение двух чисел:
      def multiply(a, b):
       return a * b
   

### Задачи

1. Напишите функцию, которая вычисляет максимальное из трёх чисел.
def max_of_three(a, b, c):
    return max(a, b, c)


2. Напишите функцию, которая вычисляет сразу максимальное и минимальное из трёх чисел.
def min_max_of_three(a, b, c):
    return (min(a, b, c), max(a, b, c))


3. Напишите функцию, которая вычисляет количество цифр числа.
def count_digits(n):
    return len(str(abs(n)))  # abs для обработки отрицательных чисел


4. Напишите функцию, которая вычисляет наибольший общий делитель двух чисел.
def gcd(a, b):
    while b:
        a, b = b, a % b
    return a


5. Напишите функцию, которая вычисляет наименьшее общее кратное двух чисел.
def lcm(a, b):
    return abs(a * b) // gcd(a, b)


6. Напишите функцию, которая «разворачивает» десятичную запись числа. 
def reverse_number(n):
    return int(str(n)[::-1])


7. Напишите функцию, которая моделирует бросание двух игральных кубиков.
import random

def throw_dice():
    return (random.randint(1, 6), random.randint(1, 6))


8. Напишите функцию, которая вычисляет факториал натурального числа М.
def factorial(m):
    if m == 0:
        return 1
    else:
        return m * factorial(m - 1)


9. Напишите функцию, которая вычисляет N-е число Фибоначчи.
def fibonacci(n):
    if n <= 0:
        return 0
    elif n == 1:
        return 1
    else:
        return fibonacci(n - 1) + fibonacci(n - 2)


10. Напишите функцию, которая находит все пары дружественных чисел.
def sum_of_divisors(n):
    return sum(i for i in range(1, n) if n % i == 0)
    def amicable_numbers(limit):
    pairs = []
    for i in range(1, limit):
        j = sum_of_divisors(i)
        if j < limit and i != j and sum_of_divisors(j) == i:
            pairs.append((i, j))
    return pairs


11. Напишите программу, которая находит все числа на отрезке 0, N, сумма цифр которых не меняется при умножении на 2, 3, 4, 5, 6, 7, 8 и 9.
def digit_sum(n):
    return sum(int(digit) for digit in str(n))

def find_same_digit_sum(N):
    result = []
    for i in range(N + 1):
        if all(digit_sum(i) == digit_sum(i * j) for j in range(2, 10)):
            result.append(i)
    return result


12. Напишите логическую функцию, которая определяет, является ли число совершенным.
def is_perfect(n):
    return n == sum(i for i in range(1, n) if n % i == 0)


13. Напишите логическую функцию, которая определяет, является ли число гиперпростым.
def is_prime(num):
    if num < 2:
        return False
    for i in range(2, int(num**0.5) + 1):
        if num % i == 0:
            return False
    return True

def is_hyperprime(n):
    str_n = str(n)
    # Проверяем все возможные числа, которые можно получить, удалив цифры
    for i in range(len(str_n)):
        for j in range(i+1, len(str_n) + 1):
            if not is_prime(int(str_n[i:j])):
                return False
    return True

### Ответы на вопросы
### параграф 61

1. Что такое рекурсия? Приведите примеры.
   Рекурсия — это метод, при котором функция вызывает саму себя для решения более мелких подзадач. Примером рекурсивной функции является вычисление факториала:
      Факториал(n) = n * Факториал(n-1), если n > 1
   Факториал(1) = 1
   

2. Почему любое рекурсивное определение состоит из двух частей?
   Рекурсивное определение состоит из двух частей: базового случая (условия, при котором рекурсия останавливается) и рекурсивного случая (где функция вызывает саму себя для решения подзадачи). Это необходимо для предотвращения бесконечной рекурсии и обеспечения завершенности.

3. Что такое рекурсивная процедура (функция)?
   Рекурсивная процедура или функция — это такая, которая вызывает саму себя в своем теле. Например, функция для вычисления чисел Фибоначчи:
      Фиб(n) = Фиб(n-1) + Фиб(n-2) при n > 1
   Фиб(0) = 0, Фиб(1) = 1
   

4. Расскажите о задаче «Ханойские башни». Попытайтесь придумать алгоритм её решения, не использующий рекурсию.
   Задача «Ханойские башни» состоит в том, чтобы переместить набор дисков с одного стержня на другой, используя третий стержень, при условии, что больше дисков нельзя помещать на меньшие. Рекурсивное решение заключается в перемещении n-1 дисков, а затем перемещении n-го диска.

   Нерекурсивный алгоритм требует использования стека или очереди для отслеживания перемещений. Можно воспользоваться итеративным подходом и посчитать количество перемещений, а затем воспользоваться битовыми операциями для выяснения, какой диск стоит переместить на каждом этапе.

5. Процедура А вызывает процедуру Б, а процедура Б — процедуру А и саму себя. Какую из этих процедур можно назвать рекурсивной?
   Процедуру Б можно назвать рекурсивной, если она вызывает саму себя. Процедура А может быть взаиморекурсивной, если она вызывает процедуру Б, а та уже вызывает А.

6. В каком случае рекурсия никогда не остановится? Докажите, что в рассмотренных в параграфе задачах этого не случится.
   Рекурсия никогда не остановится, если отсутствует базовый случай или условие, при котором рекурсия завершается. Например, если функция всегда вызывает себя с одинаковыми параметрами, это приведет к бесконечной рекурсии. В задачах, рассмотренных в параграфе, базовые случаи со строгими условиями (например, 0 для факториала) предотвратят бесконечность.

7. Что такое стек? Как он используется при выполнении программ?
   Стек — это структура данных, работающая по принципу LIFO (последний пришел — первый вышел). В программировании стек используется для хранения контекста выполнения функций, включая локальные переменные и адрес возврата, что позволяет осуществлять управление памятью и выполнять рекурсию.

8. Почему при использовании рекурсии может случиться переполнение стека?
   Переполнение стека может произойти, если функции вызывают друг друга слишком много раз без достижения базового случая. Это приводит к тому, что стек затаскивает все больше и больше уровней вызова, что в конечном итоге приводит к недостатку памяти.

9. Назовите достоинства и недостатки рекурсии. Когда её следует использовать, а когда нет?
   Достоинства:
   - Упрощение кода и логики задач, особенно для структур, таких как деревья и графы.
   - Чистота и ясность алгоритмов.

   Недостатки:
   - Возможное переполнение стека.
   - Более высокие затраты на память и вычислительные ресурсы.
   - Иногда может быть сложнее проанализировать производительность.

   Рекурсию следует использовать при решении задач, которые естественно разбиваются на подзадачи (например, сортировка, обход деревьев). Не стоит использовать рекурсию, если известно, что глубина рекурсии может быть значительной или когда производительность критична.

### Сообщения

а) Фракталы
   Фракталы — это геометрические фигуры, которые показывают самоподобие на разных масштабах. Они могут быть созданы с помощью простых рекурсивных алгоритмов. Пример фрактала — треугольник Серпинского, который разделяется на более мелкие треугольники.

б) Числа ФибоначчиЧисла Фибоначчи — это последовательность, в которой каждое число является суммой двух предыдущих, начиная с 0 и 1. Они часто появляются в природе, в архитектуре и в искусстве.

в) Рекурсия вокруг нас
   Рекурсия присутствует в природе (например, в структуре растений) и в архитектуре (фракталы, самоподобные узоры). Рекурсия помогает моделировать сложные системы и создавать алгоритмы для их анализа.

г) Рекурсия в программировании: за и против
   Рекурсия позволяет упростить написание кода, особенно для задач, связанных с иерархическими структурами. Однако она требует осторожности из-за потенциального переполнения стека и возможной большой вычислительной нагрузки.

д) Рекурсия в произведениях искусства
   Рекурсивные паттерны можно увидеть в праздниках, архитектурных стилях и даже в музыке. Художники иногда используют фрактальные методы для создания своих произведений, что приводит к необычным и завораживающим структурам.

### Задачи

1. Придумайте свою рекурсивную фигуру и опишите её.
   Примером рекурсивной фигуры может быть фрактал «дерево». Это дерево строится путем отрисовки ствола и разветвлений, где каждое ветвление также может быть представлено как еще одно дерево. Каждый уровень деревьев уменьшает длину ствола и угол наклона.

3. Напишите рекурсивную процедуру для перевода числа в двоичную систему.
      def to_binary(n):
       if n > 1:
           to_binary(n // 2)
       print(n % 2, end='')

   to_binary(10)  # Вывод: 1010
   
5. Напишите рекурсивную процедуру для перевода числа из двоичной системы в десятичную.
      def binary_to_decimal(n):
       if n == 0:
           return 0
       else:
           return (n % 10) + 2 * binary_to_decimal(n // 10)

   print(binary_to_decimal(1010))  # Вывод: 10
