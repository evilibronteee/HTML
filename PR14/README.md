# Практическая работа №14 #

### Тема: Использование одномерных массивов на Javascript

#### Ход работы

#### Задача:

### ЗАДАНИЕ 1. 
### Вариант 8.	Оценки, полученные спортсменом в соревнованиях по фигурному катанию (в баллах), хранятся в массиве из 8 элементов. В первых трех элементах записаны оценки по обязательной программе, с 4 по 6 — по короткой программе, в остальных — по произвольной про¬грамме. Выяснить, по какому виду программы спортсмен показал лучший результат.


### Код программы:

### (zd1.html)

```
<!DOCTYPE html>
<html>
<head>
    <title>Оценки Фигурного Катания</title>
</head>
<body>
    <h2>Введите оценки фигурного катания</h2>

    <h3>Обязательная программа</h3>
    <input type="number" id="score1" placeholder="Оценка 1" required>
    <input type="number" id="score2" placeholder="Оценка 2" required>
    <input type="number" id="score3" placeholder="Оценка 3" required>

    <h3>Короткая программа</h3>
    <input type="number" id="score4" placeholder="Оценка 4" required>
    <input type="number" id="score5" placeholder="Оценка 5" required>
    <input type="number" id="score6" placeholder="Оценка 6" required>

    <h3>Произвольная программа</h3>
    <input type="number" id="score7" placeholder="Оценка 7" required>
    <input type="number" id="score8" placeholder="Оценка 8" required>

    <!-- Кнопка для расчета -->
    <button onclick="findBestProgram()">Вычислить лучшую программу</button>

    <!-- Место для отображения результата -->
    <p id="result"></p>

    <script>
        function findBestProgram() {
            var scores = [];
            for (var i = 1; i <= 8; i++) {
                scores.push(parseFloat(document.getElementById('score' + i).value));
            }

            // Тот же код, что был представлен ранее
            var mandatorySum = scores[0] + scores[1] + scores[2];
            var shortSum = scores[3] + scores[4] + scores[5];
            var freeSum = scores[6] + scores[7];

            var mandatoryAverage = mandatorySum / 3;
            var shortAverage = shortSum / 3;
            var freeAverage = freeSum / 2;

            var bestProgram = '';
            var highestScore = 0;

            if (mandatoryAverage > highestScore) {
                bestProgram = 'Обязательная программа';
                highestScore = mandatoryAverage;
            }

            if (shortAverage > highestScore) {
                bestProgram = 'Короткая программа';
                highestScore = shortAverage;
            }

            if (freeAverage > highestScore) {
                bestProgram = 'Произвольная программа';
                highestScore = freeAverage;
            }

            document.getElementById('result').innerHTML = 'Лучшая программа: ' + bestProgram;
        }
    </script>
</body>
</html>

```
### Задание 2. Выполните 1 задания – номер первого задания – это ваш номер по журналу. Количество элементов N – произвольное и вводится с клавиатуры, значение элементов массива генерируются случайным образом, кроме контрольных примеров, когда значения массива инициализируются присваиванием. 
### Вариант 8
В одномерном массиве, состоящем из п вещественных элементов, вычислить:
1.	Номер минимального элемента массива.
2.	Сумму элементов массива, расположенных между первым и вторым отрица¬тельными элементами.


### zd2.html

```
<!DOCTYPE html>
<html>
<head>
    <title>Задание с массивами</title>
    <script>
        function generateArray(n) {
            let array = [];
            for (let i = 0; i < n; i++) {
                // Генерируем случайные числа в диапазоне от -5 до 5 и округляем до сотых
                array.push((Math.random() * 10 - 5).toFixed(2));
            }
            return array;
        }

        function findMinElementIndex(array) {
            // Преобразуем строки обратно в числа для поиска минимального значения
            let numericArray = array.map(Number);
            return numericArray.indexOf(Math.min(...numericArray));
        }

        function sumBetweenNegatives(array) {
            let numericArray = array.map(Number);
            let firstNegativeIndex = numericArray.findIndex(x => x < 0);
            let secondNegativeIndex = numericArray.slice(firstNegativeIndex + 1).findIndex(x => x < 0);
            if (firstNegativeIndex !== -1 && secondNegativeIndex !== -1) {
                secondNegativeIndex += firstNegativeIndex + 1;
                let sum = numericArray.slice(firstNegativeIndex + 1, secondNegativeIndex).reduce((acc, val) => acc + val, 0);
                return sum.toFixed(2); // Округляем сумму до сотых
            } else {
                return "Недостаточно отрицательных элементов";
            }
        }

        function displayResult() {
            const n = parseInt(document.getElementById("arraySize").value);
            const array = generateArray(n);
            document.getElementById("array").innerText = "Массив: " + array.join(", ");
            document.getElementById("minIndex").innerText = "Индекс минимального элемента: " + findMinElementIndex(array);
            document.getElementById("sumBetween").innerText = "Сумма между отрицательными: " + sumBetweenNegatives(array);
        }
    </script>
</head>
<body>
    <h2>Задание с массивами</h2>
    <label for="arraySize">Введите размер массива:</label>
    <input type="number" id="arraySize" value="10">
    <button onclick="displayResult()">Генерировать и обработать массив</button>

    <h3>Результат:</h3>
    <p id="array"></p>
    <p id="minIndex"></p>
    <p id="sumBetween"></p>
</body>
</html>

```


### Результат работы программы: 
![задание1](https://github.com/evilibronteee/HTML/blob/main/PR14/%D0%9E%D1%86%D0%B5%D0%BD%D0%BA%D0%B8%20%D0%A4%D0%B8%D0%B3%D1%83%D1%80%D0%BD%D0%BE%D0%B3%D0%BE%20%D0%9A%D0%B0%D1%82%D0%B0%D0%BD%D0%B8%D1%8F%20-%20Google%20Chrome%2001.04.2024%2012_32_37.png?raw=true)

![задание2](https://github.com/evilibronteee/HTML/blob/main/PR14/%D0%97%D0%B0%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5%20%D1%81%20%D0%BC%D0%B0%D1%81%D1%81%D0%B8%D0%B2%D0%B0%D0%BC%D0%B8%20-%20Google%20Chrome%2001.04.2024%2014_21_27.png?raw=true)
