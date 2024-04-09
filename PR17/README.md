# Практическая работа №17 #

### Тема: Использование обработчиков событий на Javascript
#### Ход работы

#### Задача:

### ЗАДАНИЕ 1. 
### 8  Написать функцию, которая возвращает количество нечетных элементов массива.
### Код программы:

### (zd1.html)

```
<!DOCTYPE html>
<html>
<head>
    <title>Подсчет Нечетных Элементов Массива</title>
</head>
<body>
    <h2>Подсчет Нечетных Элементов Массива</h2>
    <input type="text" id="arrayInput" placeholder="Введите элементы массива через запятую, например: 1,2,3,4,5">
    <button onclick="countOddNumbers()">Подсчитать</button>
    <p id="result"></p>

    <script>
        function countOddNumbers() {
            var input = document.getElementById('arrayInput').value;
            // Преобразование введенной строки в массив чисел
            var arr = input.split(',').map(num => parseInt(num.trim()));

            // Фильтрация массива для выделения нечетных чисел и подсчет их количества
            var oddCount = arr.filter(number => number % 2 !== 0).length;

            document.getElementById('result').innerText = "Количество нечетных элементов: " + oddCount;
        }
    </script>
</body>
</html>

```
### Задание 2. 8  Написать функцию, которая возвращает сумму первого и последнего  нечетных элементов массива.

### zd2.html

```
<!DOCTYPE html>
<html>
<head>
    <title>Сумма Нечетных Элементов</title>
</head>
<body>
    <h2>Сумма Первого и Последнего Нечетных Элементов Массива</h2>
    <input type="text" id="arrayInput" placeholder="Введите элементы массива через запятую">
    <button onclick="sumOfOddElements()">Подсчитать</button>
    <p id="result"></p>

    <script>
        function sumOfOddElements() {
            var input = document.getElementById('arrayInput').value;
            var arr = input.split(',').map(num => parseInt(num.trim()));

            var firstOdd = null, lastOdd = null;
            for (let num of arr) {
                if (num % 2 !== 0) {
                    if (firstOdd === null) firstOdd = num;
                    lastOdd = num;
                }
            }

            if (firstOdd !== null && lastOdd !== null) {
                document.getElementById('result').innerText = 
                    "Сумма первого и последнего нечетных элементов: " + (firstOdd + lastOdd);
            } else {
                document.getElementById('result').innerText = "Нечетные элементы в массиве не найдены.";
            }
        }
    </script>
</body>
</html>
```


### Результат работы программы: 
![задание1](https://github.com/evilibronteee/HTML/blob/main/PR17/%D0%9F%D0%BE%D0%B4%D1%81%D1%87%D0%B5%D1%82%20%D0%9D%D0%B5%D1%87%D0%B5%D1%82%D0%BD%D1%8B%D1%85%20%D0%AD%D0%BB%D0%B5%D0%BC%D0%B5%D0%BD%D1%82%D0%BE%D0%B2%20%D0%9C%D0%B0%D1%81%D1%81%D0%B8%D0%B2%D0%B0%20-%20Google%20Chrome%2009.04.2024%2017_37_54.png?raw=true)

![задание2](https://github.com/evilibronteee/HTML/blob/main/PR17/%D0%A1%D1%83%D0%BC%D0%BC%D0%B0%20%D0%9D%D0%B5%D1%87%D0%B5%D1%82%D0%BD%D1%8B%D1%85%20%D0%AD%D0%BB%D0%B5%D0%BC%D0%B5%D0%BD%D1%82%D0%BE%D0%B2%20-%20Google%20Chrome%2009.04.2024%2017_42_40.png?raw=true)
