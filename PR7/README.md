# Практическая работа №8 #

### Тема: Создание связанных Web-страницм

#### Ход работы

#### Задача:

**Задание.   С помощью тегов в текстовом редакторе БЛОКНОТ создайте 3-4 взаимосвязанные электронные страницы. Поместите на них необходимую текстовую информацию, рисунки , таблицы, формы для заполнения,  элементы оформления, продумайте цветовое оформление и свяжите с помощью гиперссылок.
Обязательные элементы:
1 страница – Титульная – помещаем информацию о теме, авторе, список страниц с гиперссылками, тематический рисунок.
2 страница – Основная – помещает текстовую информацию с использованием разных типов шрифтов и заголовков, заполненную таблицу (4 столбца*3 строки), тематический рисунок с ссылкой на 3 страницу.
3 страница – Дополнительная – помещаем формы для заполнения общей информацией или  оформления заказа, используем все разновидности полей ввода.
4 страница – содержимое и оформление продумайте самостоятельно.**

### Вариант-8   WEB-сайт «Любимые книги»

### Код программы:

### 1 страница(index.html)

```
<!DOCTYPE html>
<html>
<head>
    <title>Любимые книги - Главная</title>
    <link rel="stylesheet" type="text/css" href="style.css">
</head>
<body>
    <header>
        <h1>Любимые книги</h1>
        <p>Автор: Виктория Гребенюк</p>
    </header>
    <nav>
        <ul>
            <li><a href="main.html" target="_self">Каталог книг</a></li>
            <li><a href="additional.html" target="_self">Обратная связь</a></li>
            <li><a href="custom.html" target="_self">О проекте</a></li>
        </ul>
    </nav>
    <img src="book-theme.jpg" alt="Тематическое изображение книг">
</body>
</html>
```
### 2 страница(main.html)
```
<!DOCTYPE html>
<html>
<head>
    <title>Каталог книг</title>
    <link rel="stylesheet" type="text/css" href="style.css">
</head>
<body>
    <h2>Каталог любимых книг</h2>
    <p>Здесь вы найдете информацию о лучших книгах...</p>
    <table>
        <tr>
            <th>Название</th>
            <th>Автор</th>
            <th>Жанр</th>
            <th>Год издания</th>
        </tr>
        <<tr>
            <td>Акция №1</td>
            <td>Джерри Сигел</td>
            <td>1938</td>
            <td>Первое появление Супермена.</td>
        </tr>
        <tr>
            <td>Смерть Супермена</td>
            <td>Дэн Жургенс</td>
            <td>1992</td>
            <td>Эпическая битва с Думсдэем, в которой Супермен погибает.</td>
        </tr>
        <tr>
            <td>Супермен: Возвращение</td>
            <td>Марк Уэйд</td>
            <td>2003</td>
            <td>Переосмысление истории происхождения Супермена.</td>
        </tr>
    </table>
    <a href="additional.html"><img src="book-link.jpg" alt="Книга с ссылкой на отзывы">
	</a>
	<a href="index.html" target="_self">Вернуться на главную</a>
</body>
</html>

```

### 3 страница(additional.html)

```
<!DOCTYPE html>
<html>
<head>
    <title>Обратная связь</title>
    <link rel="stylesheet" type="text/css" href="style.css">
</head>
<body>
    <h1>Обратная связь</h1>
    <form>
        <label for="name">Ваше имя:</label>
        <input type="text" id="name" name="name"><br>
        <label for="email">Ваш email:</label>
        <input type="email" id="email" name="email"><br>
        <label for="message">Сообщение:</label>
        <textarea id="message" name="message"></textarea><br>
        <input type="submit" value="Отправить">
    </form>
	<a href="index.html" target="_self">Вернуться на главную</a>
</body>
</html>
```

### 4 страница(custom.html)

```
<!DOCTYPE html>
<html>
<head>
    <title>О проекте</title>
    <link rel="stylesheet" type="text/css" href="style.css">
</head>
<body>
    <h1>О проекте</h1>
    <p>Информация о проекте "Любимые книги" и его создателе...</p>
	<h3>Группа 3СА –05</h3>
	<h3>Выполнил студент: Гребенюк В.Д</h3>
	<a href="index.html" target="_self">Вернуться на главную</a>
</body>
</html>
```
### style.css

```
body {
    font-family: Arial, sans-serif;
    background-color: #0fc7ff;
}

h1 {
    color: #333;
}

table, th, td {
    border: 1px solid black;
    border-collapse: collapse;
}

th, td {
    padding: 8px;
    text-align: left;
}

h2{
    font-family: Times New Roman, sans-serif;
	font-style: italic;
	color: #1af061;
}
p {
	font-family: Verdana, sans-serif;
	color: #fc9208;
}
```


### Результат работы программы:
* 1 страница   
![1 страница](https://github.com/evilibronteee/HTML/blob/main/PR7/%D0%9B%D1%8E%D0%B1%D0%B8%D0%BC%D1%8B%D0%B5%20%D0%BA%D0%BD%D0%B8%D0%B3%D0%B8%20-%20%D0%93%D0%BB%D0%B0%D0%B2%D0%BD%D0%B0%D1%8F%20-%20Google%20Chrome%2022.03.2024%2016_12_36.png?raw=true)
* 2 страница  
![2 страница](https://github.com/evilibronteee/HTML/blob/main/PR7/%D0%9B%D1%8E%D0%B1%D0%B8%D0%BC%D1%8B%D0%B5%20%D0%BA%D0%BD%D0%B8%D0%B3%D0%B8%20-%20%D0%93%D0%BB%D0%B0%D0%B2%D0%BD%D0%B0%D1%8F%20-%20Google%20Chrome%2022.03.2024%2016_12_43.png?raw=true)
* 3 страница  
![3 страница](https://github.com/evilibronteee/HTML/blob/main/PR7/%D0%9B%D1%8E%D0%B1%D0%B8%D0%BC%D1%8B%D0%B5%20%D0%BA%D0%BD%D0%B8%D0%B3%D0%B8%20-%20%D0%93%D0%BB%D0%B0%D0%B2%D0%BD%D0%B0%D1%8F%20-%20Google%20Chrome%2022.03.2024%2016_12_48.png?raw=true)

* 4 страница
![4 страница](https://github.com/evilibronteee/HTML/blob/main/PR7/%D0%9B%D1%8E%D0%B1%D0%B8%D0%BC%D1%8B%D0%B5%20%D0%BA%D0%BD%D0%B8%D0%B3%D0%B8%20-%20%D0%93%D0%BB%D0%B0%D0%B2%D0%BD%D0%B0%D1%8F%20-%20Google%20Chrome%2022.03.2024%2016_12_57.png?raw=true)
