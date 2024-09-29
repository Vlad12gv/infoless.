1. Представление целых чисел со знаком и без знака в компьютере отличается способом, которым отводится бит для обозначения знака числа. В числах со знаком старший бит (знаковый бит) используется для указания знака числа - 0 для положительных чисел и 1 для отрицательных чисел. В числах без знака все биты отводятся для представления самого числа, и они могут принимать только неотрицательные значения.

2. Примеры величин, которые всегда имеют целые неотрицательные значения, включают количество предметов, количество денег, количество людей и т.д. Такие величины никогда не могут быть отрицательными.

3. Целые числа без знака в компьютере представляются прямым кодом. Каждый бит в таком числе отображает определенную степень двойки (от 2^0 до 2^(n-1)), и значение числа получается путем сложения всех этих степеней двойки, которым соответствуют установленные биты.

4. Диапазон представления чисел увеличивается с увеличением количества разрядов. Если увеличить количество разрядов на 1, то диапазон будет увеличен в два раза (возможность хранения большего числа), так как каждый новый разряд может принимать значения либо 0, либо 1. Аналогично, если увеличить количество разрядов на 2 или n, то диапазон увеличится соответственно в 4 или в 2^n раз.

5. Максимальное целое беззнаковое число, которое можно записать с K двоичных разрядов, равно (2^K - 1), так как все разряды заполнены единицами. Если прибавить единицу к этому максимальному значению, то произойдет переполнение и получится число 0.

6. При переполнении процессор обычно отбрасывает старшие разряды результата, оставляя только младшие разряды. Это может привести к искажениям данных и неправильным результатам операций.

7. Максимальное положительное и минимальное отрицательное значения у целых двоичных чисел со знаком имеют разные абсолютные значения, так как старший бит (знаковый бит) в отрицательных числах отводится для обозначения знака, а не для представления значения числа. Это приводит к смещению диапазона значений в отрицательную сторону.

8. Нет, положительные числа не кодируются одинаково в знаковом и беззнаковом форматах. В знаковом формате старший бит используется для обозначения знака числа, в то время как в беззнаковом формате все биты отводятся для представления самого числа.

9. Существуют различные алгоритмы получения дополнительного кода для отрицательного числа. Например, можно инвертировать все биты положительного числа и затем прибавить к нему единицу, чтобы получить дополнительный код этого числа.

10. Алгоритмы Al, A2 и A3 дают один и тот же результат, так как они все основаны на применении операции инверсии (побитового отрицания) и операции сложения к положительному числу.

11. Минимальное отрицательное значение, которое можно записать с K двоичных разрядов, равно -2^(K-1), так как старший бит отведен для обозначения знака (равен 1).

12. Переполнение может возникнуть при сложении двух отрицательных чисел и в этом случае знак результата будет положительным. Например, если сложить -2 и -3, то получится -5, что превышает допустимый диапазон отрицательных чисел.

13. Если правила перевода в дополнительный код применить к отрицательному числу, то получится обратный код числа с добавлением к младшему разряду единицы.

14. -

15. Если старший (знаковый) разряд числа, записанного в прямом коде, равен 0, то число положительное и никаких преобразований не делается.

16. Если старший (знаковый) разряд числа, записанного в прямом коде, равен 1, то число отрицательное, все разряды числа, кроме знакового, инвертируются, а к результату прибавляется 1.

17. Его преимущество заключается в том, что он позволяет:

18. Заменить операцию вычитания на операцию сложения;

19. Сделать операции сложения и вычитания одинаковыми для знаковых и беззнаковых чисел, что упрощает архитектуру ЭВМ.

20. В источнике говорится, что вместо вычитания в компьютере используется сложение с дополнительным кодом вычитаемого.