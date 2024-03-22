# Практическая работа №9 #

### Тема: Использование динамического HTML при работе с текстом

#### Ход работы

#### Задача:

ЗАДАНИЕ. Возьмите страницу любого текста, подключите любой шрифт  и отформатируйте его средствами CSS


### Код программы:

### (index.html)

```
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <link rel="stylesheet" href="styles.css">
    <link href="https://fonts.googleapis.com/css2?family=Chathura&display=swap" rel="stylesheet">
</head>
<body>
    <div class="text-block">
        <p class="italic-text">He really looked pale, so Harry, greatly worried, went to Madame Malkin's alone.</p>
        <p class="bold-text">She turned out to be a squat, smiling witch dressed in mauve..</p>
        <p class="large-text">"Going to Hogwarts, honey?" She interrupted his inarticulate babble. "</p>
		<p class="blue-text">Everything you need is here," and here, by the way, is another young man at the fitting. </p>
		<p class="letter-spacing">At the back of the store, a boy with a pale, sharp face was standing on a low stool, and a second witch was pinning the hem of his black robe with pins. </p>
		<p> Madame Malkin put Harry on a stool next to him, put a dress over his head and began to shorten it. </p>
    </div>
</body>
</html>
```

### style.css

```
.text-block {
    font-family: 'Chathura', sans-serif;
    font-size: 24px;
    color: #333333;
    line-height: 1.6;
    word-wrap: break-word;
    letter-spacing: 0.05em;
}

.italic-text {
    font-style: italic;
}

.bold-text {
    font-weight: bold;
}

.large-text {
    font-size: 48px;
}

.blue-text {
    color: blue;
}

.letter-spacing {
    letter-spacing: 0.1em; /* Измените это значение по вашему усмотрению */
}
```


### Результат работы программы: 
![1 страница](https://github.com/evilibronteee/HTML/blob/main/PR9/%D0%A1%D0%B6%D0%B0%D1%82%D0%B8%D0%B5%20%D0%B8%D0%B7%D0%BE%D0%B1%D1%80%D0%B0%D0%B6%D0%B5%D0%BD%D0%B8%D0%B9%20%D0%BE%D0%BD%D0%BB%D0%B0%D0%B9%D0%BD%20%D0%9D%D0%B0%D0%B8%D0%BB%D1%83%D1%87%D1%88%D0%B5%D0%B5%20%D0%BA%D0%B0%D1%87%D0%B5%D1%81%D1%82%D0%B2%D0%BE%20%D0%B8%20%D1%81%D0%B6%D0%B0%D1%82%D0%B8%D0%B5%20-%20Google%20Chrome%2022.03.2024%2018_14_49.png?raw=true)
