# Практическая работа №1 #

### Тема: Применение операции присваивания и описание переменных

#### Ход работы

#### Задача:


### 8. Стрелка прибора вращается с постоянной скоростью, совершая w оборотов в секунду (не обязательно стрелка прибора, может быть это волчок в игре «Что? Где? Когда?» и т.п.) Угол поворота стрелки в нулевой момент времени примем за 0. Каков будет угол поворота через t секунд?
### Код программы:

### (index.html)

```
<!DOCTYPE html>
<html>
<head>
    <title>Угол поворота</title>
    <script>
        function calculateAngle() {
            let w = parseFloat(document.getElementById("w").value); // количество оборотов в секунду
            let t = parseFloat(document.getElementById("t").value); // время в секундах

            let angle = w * t * 360; // вычисление угла

            document.getElementById("result").innerText = "Угол поворота: " + angle.toFixed(2) + " градусов";
        }
    </script>
</head>
<body>
    <h2>Угол поворота стрелки прибора или волчка</h2>
    <label for="w">Оборотов в секунду (w):</label>
    <input type="number" id="w"><br>
    <label for="t">Время в секундах (t):</label>
    <input type="number" id="t"><br>
    <button onclick="calculateAngle()">Вычислить угол</button>
    <p id="result"></p>
</body>
</html>


```




### Результат работы программы: 

![](https://github.com/evilibronteee/HTML/blob/main/PR1_YP/%D0%A3%D0%B3%D0%BE%D0%BB%20%D0%BF%D0%BE%D0%B2%D0%BE%D1%80%D0%BE%D1%82%D0%B0%20-%20Google%20Chrome%2006.04.2024%2013_06_31.png?raw=true)
