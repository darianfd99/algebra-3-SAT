# Задание: 3-однородные множества и задача 3<sub>>=7/8</sub>‑ВЫПОЛНИМОСТЬ

Частичный зачёт сданных с опозданием решений не предусмотрен. Решения на Python должны соответствовать стандарту PEP8. По решениям на других языках см. гайдлайны Google: C++, Java. Для языка Scala есть официальные гайдлайны. В крайнем случае, используйте другие гайдлайны, указывая на них ссылку в комментариях в шапке Вашего исходника. Перед сдачей прогоняйте свои исходники через линтеры (linters), чтобы не оставалось неиспользованных переменных и функций, а также других огрехов, которые линтеры замечают.

Реализуйте алгоритм, который, используя построенное на лекции 3-однородное множество наборов, находит решение задачи 
3<sub>>=7/8</sub>‑ВЫПОЛНИМОСТЬ.

На вход программы подаются через пробел два числа n и m — число переменных и число скобок соответственно, а далее подаются
m строк, кодирующих клаузы, в формате:

```input
<neg>var1 <neg>var2 <neg>var3
…
```

где на месте <neg> может быть либо пустая строка, либо дефис, который означает отрицание соответствующей переменной. При этом на месте var1/var2/var3 стоят числа от 1 до n.

На выходе программа выдаёт единственную строку, содержащую без пробелов информацию о том, какие битовые значения можно присвоить переменным, так, чтобы как минимум 7/8 ⋅m клауз обратились в единицу (true). Проследите, что используемая для построения однородного множества наборов матрица в точности такая, как описано в лекции: столбцы упорядочены лексикографически; каждый столбец начинается с единицы, за которой следует двоичная запись номера столбца; нумерация ведётся с нуля.

### Sample Input 1:

```input
2 2
1 -1 2
-1 2 -2
```

### Sample Output 1:

```output
00
```
___

### Sample Input 2:

```input
3 6
-1 -2 -3
-1 -2 3
1 -2 -3
1 -2 3
1 2 -3
1 2 3
```

### Sample Output 2:

```output
101
```