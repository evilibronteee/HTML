# Практическая работа №12 #

### Тема: Организация  множественного выбора на Javascript

#### Ход работы

#### Задача:

### 8.	Написать программу, которая по введенному номе¬ру месяца (числу от 1 до 12) выводит все приходящиеся на этот месяц праздничные дни (например, если введено число 1, то должно получиться 1 января — Новый год, 7 января — Рождество).(по 2 праздника в месяц)


### Код программы:

### (index.html)

```
<!DOCTYPE html>
<html>
<head>
    <title>Праздничные дни месяца</title>
    <script>
        function showHolidays() {
            var month = document.getElementById("monthInput").value;
            var holidays = "";
            switch (month) {
                case "1":
                    holidays = "1 января — Новый год, 7 января — Рождество";
                    break;
                case "2":
                    holidays = "14 февраля — День всех влюбленных, 23 февраля — День защитника Отечества";
                    break;
                case "3":
                    holidays = "8 марта — Международный женский день, последний день марта — Переход на летнее время";
                    break;
                case "4":
                    holidays = "1 апреля — День смеха, 12 апреля — День космонавтики";
                    break;
                case "5":
                    holidays = "1 мая — Праздник Весны и Труда, 9 мая — День Победы";
                    break;
                case "6":
                    holidays = "1 июня — День защиты детей, 12 июня — День России";
                    break;
                case "7":
                    holidays = "7 июля — Иван Купала, последнее воскресенье июля — День Военно-Морского Флота";
                    break;
                case "8":
                    holidays = "Первый день августа — День железнодорожника, последний день августа — День знаний";
                    break;
                case "9":
                    holidays = "Первый понедельник сентября — День знаний, третье воскресенье сентября — День избирателя";
                    break;
                case "10":
                    holidays = "1 октября — День пожилых людей, 4 октября — День учителя";
                    break;
                case "11":
                    holidays = "4 ноября — День народного единства, 7 ноября — День Октябрьской революции";
                    break;
                case "12":
                    holidays = "12 декабря — День Конституции РФ, 31 декабря — Канун Нового Года";
                    break;
                default:
                    holidays = "Неверный номер месяца";
            }
            document.getElementById("holidays").innerText = holidays;
        }
    </script>
</head>
<body>
    <h2>Праздничные дни месяца</h2>
    <label for="monthInput">Введите номер месяца (1-12):</label>
    <input type="text" id="monthInput">
    <button onclick="showHolidays()">Показать праздники</button>
    <p id="holidays"></p>
</body>
</html>


```

### Результат работы программы: 
![](https://github.com/evilibronteee/HTML/blob/main/PR12/%D0%9F%D1%80%D0%B0%D0%B7%D0%B4%D0%BD%D0%B8%D1%87%D0%BD%D1%8B%D0%B5%20%D0%B4%D0%BD%D0%B8%20%D0%BC%D0%B5%D1%81%D1%8F%D1%86%D0%B0%20-%20Google%20Chrome%2002.04.2024%2018_28_42.png?raw=true)


