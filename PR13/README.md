# Практическая работа №13 #

### Тема: Организация циклов на Javascript

#### Ход работы

#### Задача:

+	Задание 1
Вычислить и вывести на экран в виде таблицы значения функции, заданной аналитически (уравнение функции составить самостоятельно в виде дробного выражения и) , на интервале от хнач до хкон с шагом dx. Интервал и шаг задать таким образом, чтобы проверить деление на ноль и нормальный просчет значений функции. Таблицу снабдить заголовком и шапкой.

+	Задание 2 Выполните одно задание по своему варианту (использовать while). 	Дано натуральное число п. Вычислить S=1-1/2+1/4-1/8+...+(-1)^n⋅1/2^n 
+	Задание 3 Выполните одно задание по своему варианту (использовать for). 8.	Написать программу, которая вводит с клавиатуры 5 дроб¬ных чисел и вычисляет их среднее арифметическое.  



### Код программы:

### (zd1)

```

<html>
<head>
<title>Таблица значений функции</title>
</head>
<body>
<h3>Таблица значений функции f(x) = 1 / (x^2 - 1)</h3>
<table border="1">
<tr><th>x</th><th>f(x)</th></tr>
<script>
    function calculateFunction(x) {
        return 1 / (Math.pow(x, 2) - 1);
    }

    var start = -2;
    var end = 2;
    var step = 0.5;

    for (var x = start; x <= end; x += step) {
        var value;
        if (x == 1 || x == -1) {
            value = "Не определено (деление на ноль)";
        } else {
            value = calculateFunction(x).toFixed(2);
        }
        document.write("<tr><td>" + x.toFixed(2) + "</td><td>" + value + "</td></tr>");
    }
</script>
</table>
</body>
</html>
```


### (zd2)

```
<html>
<head>
<title>Сумма ряда</title>
</head>
<body>
<h3>Вычисление суммы ряда: S = 1 - 1/2 + 1/4 - 1/8 + ... + (-1)^n * 1/2^n</h3>
<script>
    var n = prompt("Введите натуральное число n:", "5"); // Пользователь вводит значение n
    n = parseInt(n);
    
    var sum = 0;
    var sign = 1; // Начальный знак

    var i = 0;
    while (i <= n) {
        sum += sign * 1/Math.pow(2, i);
        sign *= -1; // Переключение знака
        i++;
    }

    document.write("Сумма ряда при n = " + n + " равна: " + sum.toFixed(4));
</script>
</body>
</html>

```


### (zd3)

```
<html>
<head>
<title>Среднее арифметическое дробных чисел</title>
</head>
<body>
<h3>Вычисление среднего арифметического 5 дробных чисел</h3>
<script>
    var sum = 0;
    var count = 5;

    for (var i = 0; i < count; i++) {
        var num = parseFloat(prompt("Введите дробное число " + (i + 1) + ":"));
        sum += num;
    }

    var average = sum / count;
    document.write("Среднее арифметическое введенных чисел: " + average.toFixed(2));
</script>
</body>
</html>

```

### Результат работы программы: 

![задание 1](https://github.com/evilibronteee/HTML/blob/main/PR13/1.png?raw=true)

![задание 2](https://github.com/evilibronteee/HTML/blob/main/PR13/2.png?raw=true)

![задание 2](https://github.com/evilibronteee/HTML/blob/main/PR13/3.png?raw=true)



![задание 3](https://github.com/evilibronteee/HTML/blob/main/PR13/4.png?raw=true)

![задание 3](https://github.com/evilibronteee/HTML/blob/main/PR13/5.png?raw=true)

![задание 3](https://github.com/evilibronteee/HTML/blob/main/PR13/6.png?raw=true)

![задание 3](https://github.com/evilibronteee/HTML/blob/main/PR13/7.png?raw=true)

![задание 3](https://github.com/evilibronteee/HTML/blob/main/PR13/8.png?raw=true)

![задание 3](https://github.com/evilibronteee/HTML/blob/main/PR13/9.png?raw=true)