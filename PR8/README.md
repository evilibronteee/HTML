# Практическая работа №10 #

### Тема: Использование динамического HTML при работе с эффектами

#### Ход работы

#### Задача:

ЗАДАНИЕ. Возьмите страницу любого текста, подключите любой шрифт  и отформатируйте его средствами CSS


### Код программы:

### (index.html)

```
<!DOCTYPE html>
<html>
<head>
    <title>Wave Effect on Image</title>
    <style>
        #myImage {
            animation: waveAnimation 5s infinite;
            display: block;
            margin: auto;
        }

        @keyframes waveAnimation {
            0%, 100% {
                transform: scaleX(1) scaleY(1);
            }
            50% {
                transform: scaleX(1.05) scaleY(0.95);
            }
        }
    </style>
</head>
<body>
    <img id="myImage" src="https://github.com/evilibronteee/HTML/blob/main/PR10/book-theme.jpg?raw=true" alt="Книжная тематика">
</body>
</html>

```


### Результат работы программы: 
![Картинка анимирована на скриншоте это не видно](https://github.com/evilibronteee/HTML/blob/main/PR10/Wave%20Effect%20on%20Image%20-%20Google%20Chrome%2023.03.2024%2012_59_18.png?raw=true)
