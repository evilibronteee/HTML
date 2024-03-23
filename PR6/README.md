# Практическая работа №6 #

### Тема: Применение вложенных таблиц  

#### Ход работы

#### Задача:

Задание 1. Создайте 2 таблицы – в первой поместите данные о продаже и покупке трех основных валют (Евро, Доллар и Йена) любыми пятью банками, для ввода данных использовать формы. Во вторую таблицу поместите данные о максимальной покупке и минимальной продаже валют, среднему курсу продажи и покупке (см. образец). Оформление выбрать самостоятельно.

Задание 2. Создайте вложенную таблицу с использованием фонового рисунка по варианту


### Код программы:

### Задание 1(index.html)

```
<table border="1">
  <caption>Курсы валют в банках</caption>
  <tr>
    <th>Банк</th>
    <th>Покупка Евро (EUR)</th>
    <th>Продажа Евро (EUR)</th>
    <th>Покупка Доллара (USD)</th>
    <th>Продажа Доллара (USD)</th>
    <th>Покупка Йены (JPY)</th>
    <th>Продажа Йены (JPY)</th>
  </tr>
  <tr>
    <td>Сбербанк</td>
    <td>101,60 руб.</td>
    <td>108,20 руб.</td>
    <td>94 руб.</td>
    <td>97,50 руб.</td>
    <td>0,61 руб.</td>
    <td>0,67 руб.</td>
  </tr>
  <tr>
    <td>Газпромбанк</td>
    <td>99,20 руб.</td>
    <td>104,10 руб.</td>
    <td>92 руб.</td>
    <td>96,40 руб.</td>
    <td>0,51 руб.</td>
    <td>0,55 руб.</td>
  </tr>
  <tr>
    <td>Банк Открытие</td>
    <td>100,20 руб.</td>
    <td>108,10 руб.</td>
    <td>92 руб.</td>
    <td>98,45 руб.</td>
    <td>0,56 руб.</td>
    <td>0,59 руб.</td>
  </tr>
</table>

 <table border="1">
  <caption>Сводные данные по валютам</caption>
  <tr>
    <th>Валюта</th>
    <th>Максимальная покупка</th>
    <th>Минимальная продажа</th>
    <th>Средний курс покупки</th>
    <th>Средний курс продажи</th>
  </tr>
  <tr>
    <td>USD</td>
    <td>94,01 руб.</td>
    <td>91 руб.</td>
    <td>92,61 руб.</td>
    <td>92,80 руб.</td>
  </tr>
  <tr>
    <td>EUR</td>
    <td>102,70 руб.</td>
    <td>120,40 руб.</td>
    <td>100,22 руб.</td>
    <td>100,29 руб.</td>
  </tr>
  <tr>
    <td>JPY</td>
    <td>0,64 руб.</td>
    <td>0,64 руб.</td>
    <td>0,61 руб.</td>
    <td>0,65 руб.</td>
  </tr>
</table>


```

### Задание2(main.html)

```
<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<title>Вложенная таблица</title>
<style>
  .main-table { 
    border-collapse: collapse; 
    width: 100%; 
  }
  .main-table th, .main-table td { 
    border: 1px solid black; 
    padding: 10; 
  }
  .nested-table { 
    border-collapse: collapse; 
    margin: 0; 
    width: 80%; 
    height: 50%; 
  }
  .nested-table td { 
    border: 1px solid black; 
    padding: 5px; 
    text-align: center; 
  }
</style>
</head>
<body>

<table class="main-table">
  <tr>
    <th colspan="3">
      <table class="nested-table">
        <tr><td>Заголовок для всех столбцов</td></tr>
      </table>
    </th>
  </tr>
  <tr>
    <td>
      <table class="nested-table">
        <tr><td>000</td></tr>
      </table>
    </td>
    <td>
      <table class="nested-table">
        <tr><td>001</td></tr>
      </table>
    </td>
    <td>
      <table class="nested-table">
        <tr><td>Столбец 3</td></tr>
      </table>
    </td>
  </tr>
  <tr>
    <td>
      <table class="nested-table">
        <tr><td>010</td></tr>
      </table>
    </td>
    <td>
      <table class="nested-table">
        <tr><td>011</td></tr>
      </table>
    </td>
    <td>
      <table class="nested-table">
        <tr><td>002</td></tr>
      </table>
    </td>
  </tr>
  <tr>
    <td>
      <table class="nested-table">
        <tr><td>100</td></tr>
      </table>
    </td>
    <td>
      <table class="nested-table">
        <tr><td>101</td></tr>
      </table>
    </td>
    <td>
      <table class="nested-table">
        <tr><td>102</td></tr>
      </table>
    </td>
  </tr>
</table>

</body>
</html>

```


### Результат работы программы: 
![Задание1](https://github.com/evilibronteee/HTML/blob/main/PR6/2.png?raw=true)
![Задание2](https://github.com/evilibronteee/HTML/blob/main/PR6/1.png?raw=true)
