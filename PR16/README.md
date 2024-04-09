# Практическая работа №16 #

### Тема: Использование условий на Javascript

#### Ход работы

#### Задача:

### ЗАДАНИЕ 1. 
### 8 Дан диаметр круга и стороны прямоугольника. Вывести на экран площадь фигуры с меньшим периметром.
### Код программы:

### (zd1.html)

```
<!DOCTYPE html>
<html>
<head>
    <title>Задача 8</title>
</head>
<body>
    <h2>Сравнение площадей фигур</h2>
    <form id="form">
        <label>Диаметр круга:</label>
        <input type="number" id="diameter"><br>
        <label>Сторона a прямоугольника:</label>
        <input type="number" id="side_a"><br>
        <label>Сторона b прямоугольника:</label>
        <input type="number" id="side_b"><br>
        <button type="button" onclick="calculateArea()">Вычислить</button>
    </form>
    <p id="result"></p>

    <script>
        function calculateArea() {
            var diameter = parseFloat(document.getElementById('diameter').value);
            var sideA = parseFloat(document.getElementById('side_a').value);
            var sideB = parseFloat(document.getElementById('side_b').value);

            // Расчет периметров и площадей
            var perimeterCircle = Math.PI * diameter;
            var areaCircle = Math.PI * Math.pow(diameter / 2, 2);
            var perimeterRectangle = 2 * (sideA + sideB);
            var areaRectangle = sideA * sideB;

            // Определение фигуры с меньшим периметром и вычисление площади
            if (perimeterCircle < perimeterRectangle) {
                document.getElementById('result').innerHTML = 'Площадь круга: ' + areaCircle.toFixed(2);
            } else if (perimeterCircle > perimeterRectangle) {
                document.getElementById('result').innerHTML = 'Площадь прямоугольника: ' + areaRectangle.toFixed(2);
            } else {
                document.getElementById('result').innerHTML = 'Площади равны: ' + areaCircle.toFixed(2);
            }
        }
    </script>
</body>
</html>
```
### Задание 2. 8. Среди элементов случайно сгенерированного массива N целых чисел из диапазона 0 … 20 найти индекс элемента, наиболее близкого к среднему. Элементы массива должны быть выведены на экране

### zd2.html

```
<!DOCTYPE html>
<html>
<head>
    <title>Ближайший к Среднему Элемент</title>
</head>
<body>
    <h2>Найти элемент массива, ближайший к среднему значению</h2>
    <label for="arraySize">Размер массива N:</label>
    <input type="number" id="arraySize" min="1" max="100">
    <button onclick="findClosestToAverage()">Найти</button>
    <p id="arrayOutput"></p>
    <p id="result"></p>

    <script>
        function findClosestToAverage() {
            var n = parseInt(document.getElementById('arraySize').value);
            var arr = Array.from({length: n}, () => Math.floor(Math.random() * 21));
            document.getElementById('arrayOutput').innerText = 'Массив: ' + arr.join(', ');

            var average = arr.reduce((sum, val) => sum + val, 0) / n;
            var closestIndex = arr.reduce((closestIdx, current, idx) => 
                Math.abs(current - average) < Math.abs(arr[closestIdx] - average) ? idx : closestIdx, 0);

            document.getElementById('result').innerText = 
                'Индекс элемента, ближайшего к среднему (' + average.toFixed(2) + '): ' + closestIndex;
        }
    </script>
</body>
</html>
```

### Задание 3. 8.	Двумерный массив преобразовать в одномерный (размерности задаются). Оба массива вывести на экран
```
<!DOCTYPE html>
<html>
<head>
    <title>Преобразование Двумерного Массива</title>
</head>
<body>
    <h2>Преобразование Двумерного в Одномерный Массив</h2>
    <input type="number" id="rows" min="1" value="3"> x
    <input type="number" id="cols" min="1" value="3">
    <button onclick="convertArray()">Преобразовать</button>
    <p><b>Двумерный массив:</b> <span id="twoDimArray"></span></p>
    <p><b>Одномерный массив:</b> <span id="oneDimArray"></span></p>

    <script>
        function convertArray() {
            var rows = parseInt(document.getElementById('rows').value);
            var cols = parseInt(document.getElementById('cols').value);
            var twoDimArray = Array.from({length: rows}, () => 
                              Array.from({length: cols}, () => Math.floor(Math.random() * 100)));

            document.getElementById('twoDimArray').innerText = '[' + 
                twoDimArray.map(row => '[' + row.join(', ') + ']').join(', ') + ']';
            document.getElementById('oneDimArray').innerText = twoDimArray.flat().join(', ');
        }
    </script>
</body>
</html>
```

### Результат работы программы: 
![задание1](https://github.com/evilibronteee/HTML/blob/main/PR16/%D0%97%D0%B0%D0%B4%D0%B0%D1%87%D0%B0%208%20-%20Google%20Chrome%2009.04.2024%2016_56_34.png?raw=true)

![задание2](https://github.com/evilibronteee/HTML/blob/main/PR16/%D0%91%D0%BB%D0%B8%D0%B6%D0%B0%D0%B9%D1%88%D0%B8%D0%B9%20%D0%BA%20%D0%A1%D1%80%D0%B5%D0%B4%D0%BD%D0%B5%D0%BC%D1%83%20%D0%AD%D0%BB%D0%B5%D0%BC%D0%B5%D0%BD%D1%82%20-%20Google%20Chrome%2009.04.2024%2017_03_30.png?raw=true)

![задание3](https://github.com/evilibronteee/HTML/blob/main/PR16/%D0%9F%D1%80%D0%B5%D0%BE%D0%B1%D1%80%D0%B0%D0%B7%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5%20%D0%94%D0%B2%D1%83%D0%BC%D0%B5%D1%80%D0%BD%D0%BE%D0%B3%D0%BE%20%D0%9C%D0%B0%D1%81%D1%81%D0%B8%D0%B2%D0%B0%20-%20Google%20Chrome%2009.04.2024%2017_09_13.png?raw=true)