# Практическая работа №8 #

### Тема: Применение карт-изображений, использование звука и видео  в Web-страницах

#### Ход работы

#### Задача:

Создайте схематично карту супермаркета  При нажатии на отдел должно высвечиваться название отдела, товары и  акции  (все данные приблизительные)


### Код программы:

### (index.html)

```

<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Интерактивная Карта Магазина</title>
    <style>
        .modal {
            display: none;
            position: fixed;
            z-index: 1;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            overflow: auto;
            background-color: rgba(0,0,0,0.4);
            padding-top: 60px;
        }

        .modal-content {
            background-color: #fefefe;
            margin: 5% auto;
            padding: 20px;
            border: 1px solid #888;
            width: 70%;
        }

        .close {
            color: #aaa;
            float: right;
            font-size: 28px;
            font-weight: bold;
        }

        .close:hover,
        .close:focus {
            color: black;
            text-decoration: none;
            cursor: pointer;
        }
    </style>
</head>
<body>

<img src="https://github.com/evilibronteee/HTML/blob/main/PR8/Karta-fokus_1-etazh.jpg?raw=true" usemap="#supermarketMap" alt="Карта супермаркета">

<map name="supermarketMap">
 <!-- Определение активной области для М.Видео -->
    <area shape="rect" coords="18,542,263,742" href="https://github.com/evilibronteee/HTML/blob/main/PR8/mvideo_volgograd-0.jpg?raw=true" alt="М.Видео">
    
    <!-- Определение активной области для Спортмастер -->
    <area shape="rect" coords="536,548,842,728" href="https://github.com/evilibronteee/HTML/blob/main/PR8/sportmaster-2201-1.jpg?raw=true" alt="Спортмастер">
    
    <!-- Определение активной области для Мегамарт -->
    <area shape="rect" coords="69,85,405,294" href="https://github.com/evilibronteee/HTML/blob/main/PR8/mega.jpg?raw=true" alt="Мегамарт">
    
    <!-- Определение активной области для DNS -->
    <area shape="rect" coords="664,57,867,175" href="https://github.com/evilibronteee/HTML/blob/main/PR8/dns.jpg?raw=true" alt="DNS">

    <!-- Определение активной области для Ostin -->
    <area shape="rect" coords="536,424,605,514" href="https://github.com/evilibronteee/HTML/blob/main/PR8/ostin.jpg?raw=true" alt="Ostin">
</map>

<audio id="openAudio" src="https://github.com/evilibronteee/HTML/blob/main/PR8/open.mp3"></audio>
<audio id="closeAudio" src="https://github.com/evilibronteee/HTML/blob/main/PR8/close.mp3"></audio>

<div id="sportmasterModal" class="modal">
    <div class="modal-content">
        <span class="close">&times;</span>
        <h2>Спортмастер</h2>
        <!-- Встраиваем брошюру в iframe -->
        <iframe src="https://github.com/evilibronteee/HTML/blob/main/PR8/sportmaster-2201-1.jpg?raw=true" width="100%" height="600px"></iframe>
        <!-- Видеоролик -->
        <video src="204113 (540p).mp4" width="320" height="240" controls></video>
    </div>
</div>

<script>
document.querySelectorAll('area').forEach(area => {
    area.addEventListener('click', event => {
        event.preventDefault();
        var storeName = event.target.alt;
        document.querySelector('#openAudio').play();

        if (storeName === 'Спортмастер') {
            var modal = document.querySelector('#sportmasterModal');
            modal.style.display = 'block';
        } else {
            alert('Добро пожаловать в ' + storeName);
            window.open(event.target.href, '_blank');
        }
    });
});

var closeModal = document.querySelector('.close');
closeModal.onclick = function() {
    var modal = document.querySelector('#sportmasterModal');
    modal.style.display = 'none';
};

window.addEventListener('beforeunload', () => {
    document.querySelector('#closeAudio').play();
});
</script>

</body>
</html>

```


### Результат работы программы: 

![](https://github.com/evilibronteee/HTML/blob/main/PR8/%D0%98%D0%BD%D1%82%D0%B5%D1%80%D0%B0%D0%BA%D1%82%D0%B8%D0%B2%D0%BD%D0%B0%D1%8F%20%D0%9A%D0%B0%D1%80%D1%82%D0%B0%20%D0%9C%D0%B0%D0%B3%D0%B0%D0%B7%D0%B8%D0%BD%D0%B0%20-%20Google%20Chrome%2023.03.2024%2014_26_16.png?raw=true)

![](https://github.com/evilibronteee/HTML/blob/main/PR8/%D0%98%D0%BD%D1%82%D0%B5%D1%80%D0%B0%D0%BA%D1%82%D0%B8%D0%B2%D0%BD%D0%B0%D1%8F%20%D0%9A%D0%B0%D1%80%D1%82%D0%B0%20%D0%9C%D0%B0%D0%B3%D0%B0%D0%B7%D0%B8%D0%BD%D0%B0%20-%20Google%20Chrome%2023.03.2024%2014_26_20.png?raw=true)

![](https://github.com/evilibronteee/HTML/blob/main/PR8/%D0%98%D0%BD%D1%82%D0%B5%D1%80%D0%B0%D0%BA%D1%82%D0%B8%D0%B2%D0%BD%D0%B0%D1%8F%20%D0%9A%D0%B0%D1%80%D1%82%D0%B0%20%D0%9C%D0%B0%D0%B3%D0%B0%D0%B7%D0%B8%D0%BD%D0%B0%20-%20Google%20Chrome%2023.03.2024%2014_26_24.png?raw=true)

![](https://github.com/evilibronteee/HTML/blob/main/PR8/%D0%98%D0%BD%D1%82%D0%B5%D1%80%D0%B0%D0%BA%D1%82%D0%B8%D0%B2%D0%BD%D0%B0%D1%8F%20%D0%9A%D0%B0%D1%80%D1%82%D0%B0%20%D0%9C%D0%B0%D0%B3%D0%B0%D0%B7%D0%B8%D0%BD%D0%B0%20-%20Google%20Chrome%2023.03.2024%2014_26_30.png?raw=true)

![](https://github.com/evilibronteee/HTML/blob/main/PR8/%D0%98%D0%BD%D1%82%D0%B5%D1%80%D0%B0%D0%BA%D1%82%D0%B8%D0%B2%D0%BD%D0%B0%D1%8F%20%D0%9A%D0%B0%D1%80%D1%82%D0%B0%20%D0%9C%D0%B0%D0%B3%D0%B0%D0%B7%D0%B8%D0%BD%D0%B0%20-%20Google%20Chrome%2023.03.2024%2014_26_34.png?raw=true)

![](https://github.com/evilibronteee/HTML/blob/main/PR8/%D0%98%D0%BD%D1%82%D0%B5%D1%80%D0%B0%D0%BA%D1%82%D0%B8%D0%B2%D0%BD%D0%B0%D1%8F%20%D0%9A%D0%B0%D1%80%D1%82%D0%B0%20%D0%9C%D0%B0%D0%B3%D0%B0%D0%B7%D0%B8%D0%BD%D0%B0%20-%20Google%20Chrome%2023.03.2024%2014_26_43.png?raw=true)

![](https://github.com/evilibronteee/HTML/blob/main/PR8/%D0%98%D0%BD%D1%82%D0%B5%D1%80%D0%B0%D0%BA%D1%82%D0%B8%D0%B2%D0%BD%D0%B0%D1%8F%20%D0%9A%D0%B0%D1%80%D1%82%D0%B0%20%D0%9C%D0%B0%D0%B3%D0%B0%D0%B7%D0%B8%D0%BD%D0%B0%20-%20Google%20Chrome%2023.03.2024%2014_26_46.png?raw=true)

![Картинка есть, но вылетает ошибка Сайт raw.githubusercontent.com не позволяет установить соединение.](https://github.com/evilibronteee/HTML/blob/main/PR8/%D0%98%D0%BD%D1%82%D0%B5%D1%80%D0%B0%D0%BA%D1%82%D0%B8%D0%B2%D0%BD%D0%B0%D1%8F%20%D0%9A%D0%B0%D1%80%D1%82%D0%B0%20%D0%9C%D0%B0%D0%B3%D0%B0%D0%B7%D0%B8%D0%BD%D0%B0%20-%20Google%20Chrome%2023.03.2024%2014_26_53.png?raw=true)

