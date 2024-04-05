# Практическая работа №11 #

### Тема: Использование разветляющихся алгоритмов 

#### Ход работы

#### Задача:

### ЗАДАНИЕ 2. 
### Выполните задание по вариантам. В отчет поместите задание, текст программы и копию окна приложения. Использовать один из вариантов ввода данных, результат возвращать в отдельное окно.
### 8.	Подсчитать количество положительных среди чисел а, b, с

### Код программы:

### (zd1.html)

```
<!DOCTYPE html>
<html>
<head>
    <title>Подсчёт положительных чисел</title>
    <script>
        function countPositives() {
            let a = parseFloat(document.getElementById("a").value);
            let b = parseFloat(document.getElementById("b").value);
            let c = parseFloat(document.getElementById("c").value);

            let positives = 0;
            if (a > 0) positives++;
            if (b > 0) positives++;
            if (c > 0) positives++;

            document.getElementById("result").innerText = "Количество положительных чисел: " + positives;
        }
    </script>
</head>
<body>
    <h2>Подсчёт положительных чисел</h2>
    <label for="a">Введите число a:</label>
    <input type="number" id="a"><br>
    <label for="b">Введите число b:</label>
    <input type="number" id="b"><br>
    <label for="c">Введите число c:</label>
    <input type="number" id="c"><br>
    <button onclick="countPositives()">Подсчитать</button>
    <p id="result"></p>
</body>
</html>
```




### Результат работы программы: 

![задание2](https://github.com/evilibronteee/HTML/blob/main/PR11/%D0%9F%D0%BE%D0%B4%D1%81%D1%87%D1%91%D1%82%20%D0%BF%D0%BE%D0%BB%D0%BE%D0%B6%D0%B8%D1%82%D0%B5%D0%BB%D1%8C%D0%BD%D1%8B%D1%85%20%D1%87%D0%B8%D1%81%D0%B5%D0%BB%20-%20Google%20Chrome%2005.04.2024%2014_39_05.png?raw=true)
