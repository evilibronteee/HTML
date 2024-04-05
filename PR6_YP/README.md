# Практическая работа №6 #

### Тема: Использование одномерных массивов 

#### Ход работы

#### Задача:


### 8.Дана последовательность a1,a2,...,a15.Расположить элементы на четных местах по убыванию.
### Код программы:

### (index.html)

```
<!DOCTYPE html>
<html>
<head>
    <title>Сортировка элементов на четных позициях</title>
    <script>
        function sortEvenPositions() {
            // Пример массива, который можно заменить на динамический ввод
            let arr = [5, 1, 4, 3, 2, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15];

            // Извлекаем элементы на четных позициях (индексы 1, 3, 5, ...)
            let evenElements = arr.filter((_, index) => index % 2 === 1);

            // Сортировка элементов в убывающем порядке
            evenElements.sort((a, b) => b - a);

            // Обратно вставляем отсортированные элементы на четные позиции
            evenElements.forEach((element, index) => {
                arr[index * 2 + 1] = element;
            });

            // Вывод результата
            document.getElementById("result").innerText = "Отсортированный массив: " + arr.join(", ");
        }
    </script>
</head>
<body>
    <h2>Сортировка элементов на четных позициях</h2>
    <button onclick="sortEvenPositions()">Сортировать</button>
    <p id="result"></p>
</body>
</html>

```




### Результат работы программы: 

![задание2](https://github.com/evilibronteee/HTML/blob/main/PR11/%D0%9F%D0%BE%D0%B4%D1%81%D1%87%D1%91%D1%82%20%D0%BF%D0%BE%D0%BB%D0%BE%D0%B6%D0%B8%D1%82%D0%B5%D0%BB%D1%8C%D0%BD%D1%8B%D1%85%20%D1%87%D0%B8%D1%81%D0%B5%D0%BB%20-%20Google%20Chrome%2005.04.2024%2014_39_05.png?raw=true)
