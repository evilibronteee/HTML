# Практическая работа №15 #

### Тема: Использование  множественного выбора на Javascript

#### Ход работы

#### Задача:

### ЗАДАНИЕ 1. 
### Вариант 8. 8. Разработать программу, которая для введенного символа скобки ('[',']','{,'},')','(') печатает сообщение о том, является ли скобка открывающей или закрывающей, а также тип скобки (круглая, квадратная, фигурная)

### Код программы:

### (zd1.html)

```
<!DOCTYPE html>
<html>
<head>
    <title>Определение скобок</title>
    <script>
        function identifyBracket() {
            var bracket = document.getElementById("bracketInput").value;
            var message = "";
            switch (bracket) {
                case '[':
                case '{':
                case '(':
                    message = "Открывающая ";
                    break;
                case ']':
                case '}':
                case ')':
                    message = "Закрывающая ";
                    break;
                default:
                    message = "Неподходящий символ. ";
            }

            switch (bracket) {
                case '[':
                case ']':
                    message += "квадратная скобка.";
                    break;
                case '{':
                case '}':
                    message += "фигурная скобка.";
                    break;
                case '(':
                case ')':
                    message += "круглая скобка.";
                    break;
            }

            document.getElementById("result").innerText = message;
        }
    </script>
</head>
<body>
    <h2>Определение скобок</h2>
    <label for="bracketInput">Введите символ скобки ([, ], {, }, (, )):</label>
    <input type="text" id="bracketInput" maxlength="1">
    <button onclick="identifyBracket()">Определить скобку</button>
    <p id="result"></p>
</body>
</html>


```
### Задание 2. Для каждого x, изменяющегося от a до b с шагом h, найти значения функции Y(x), суммы S(x) и |Y(x)–S(x)| и вывести в виде таблицы. Значения a, b, h и n вводятся с клавиатуры. Работу программы проверить для a = 0,1; b = 1,0; h = 0,1; значение параметра n выбрать в зависимости от задания.

### zd2.html

```
<!DOCTYPE html>
<html>
<head>
    <title>Таблица функций</title>
    <script>
        function calculateAndDisplay() {
            let a = parseFloat(document.getElementById("a").value);
            let b = parseFloat(document.getElementById("b").value);
            let h = parseFloat(document.getElementById("h").value);
            let n = 8;  // Заданное значение n

            function Y(x) {
                return Math.exp(2 * x);
            }

            function S(x, n) {
                let total = 0;
                for (let k = 0; k <= n; k++) {
                    total += Math.pow(2 * x, k) / factorial(k);
                }
                return total;
            }

            function factorial(k) {
                let result = 1;
                for (let i = 2; i <= k; i++) {
                    result *= i;
                }
                return result;
            }

            let resultsTable = "<table border='1'><tr><th>x</th><th>Y(x) = e^(2x)</th><th>S(x)</th><th>|Y(x) - S(x)|</th></tr>";

            let x = a;
            while (x <= b) {
                let y = Y(x);
                let s = S(x, n);
                let diff = Math.abs(y - s);
                resultsTable += `<tr><td>${x.toFixed(2)}</td><td>${y.toFixed(2)}</td><td>${s.toFixed(2)}</td><td>${diff.toFixed(2)}</td></tr>`;
                x += h;
                x = Math.round(x * 10) / 10; 
            }

            resultsTable += "</table>";
            document.getElementById("results").innerHTML = resultsTable;
        }
    </script>
</head>
<body>
    <h2>Таблица функций Y(x) и S(x)</h2>
    <label for="a">Введите a:</label>
    <input type="number" id="a" step="0.1" value="0.1"><br>
    <label for="b">Введите b:</label>
    <input type="number" id="b" step="0.1" value="1.0"><br>
    <label for="h">Введите h:</label>
    <input type="number" id="h" step="0.1" value="0.1"><br>
    <button onclick="calculateAndDisplay()">Рассчитать и показать таблицу</button>

    <div id="results"></div>
</body>
</html>

```


### Результат работы программы: 
![задание1](https://github.com/evilibronteee/HTML/blob/main/PR15/%D0%A2%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D0%B0%20%D1%84%D1%83%D0%BD%D0%BA%D1%86%D0%B8%D0%B9%20-%20Google%20Chrome%2003.04.2024%2017_13_55.png?raw=true)

![задание2](https://github.com/evilibronteee/HTML/blob/main/PR15/%D0%A2%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D0%B0%20%D1%84%D1%83%D0%BD%D0%BA%D1%86%D0%B8%D0%B9%20-%20Google%20Chrome%2003.04.2024%2017_14_08.png?raw=true)
