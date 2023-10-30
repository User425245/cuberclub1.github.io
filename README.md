# cuberclub1.github.io
<!DOCTYPE html>
<html>
<head>
  <title>Киберклуб</title>
  <link rel="stylesheet" type="text/css" href="style.css">
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f4f4f4;
      text-align: center;
    }
    header {
      background-color: #333;
      color: #fff;
      padding: 10px 0;
    }
    nav {
      background-color: #444;
      color: #fff;
      padding: 10px 0;
    }
    section {
      padding: 20px;
    }
    footer {
      position: fixed;
      bottom: 0;
      width: 100%;
      background-color: #333;
      color: #fff;
      padding: 10px 0;
    }
	.carousel {
    display: flex;
    overflow: hidden;
    width: 300px;
    margin: 0 auto;
}

.carousel-slide {
    flex: 0 0 auto;
    width: 100%;
}

.carousel-slide img {
    width: 100%;
}

button {
    margin: 10px;
}

.background-element {
  background: url('https://cdnb.artstation.com/p/assets/images/images/057/119/045/large/ivan-fivaz-mtv-x-club-party-scene2.jpg?1670873229') no-repeat;
  background-size: cover;
  z-index: -1;
  position: relative;
}
  </style>
</head>
<body>
  <header>
    <h1>Добро пожаловать в киберклуб</h1>
  </header>
  <nav>
    <a href="#">Главная</a> |
    <a href="#">Услуги</a> |
    <a href="#">О нас</a> |
    <a href="#">Контакты</a>
  </nav>
  <section>
    <h2>Наши услуги</h2>
    <p>Мы предоставляем широкий спектр услуг по кибербезопасности и киберспорту.</p>
    <p>Наши тренеры обладают большим опытом в обучении и тренировке в области киберспорта.</p>

	<div class="carousel">
        <div class="carousel-slide">
            <img src="https://otkritkis.com/wp-content/uploads/2022/07/pdni4.gif" alt="Изображение 1">
        </div>
        <div class="carousel-slide">
            <img src="https://i.pinimg.com/originals/ce/ca/ba/cecabaac30736b17f7f278422ef861c0.gif" alt="Изображение 2">
        </div>
        <div class="carousel-slide">
            <img src="https://i.pinimg.com/originals/ce/ca/ba/cecabaac30736b17f7f278422ef861c0.gif" alt="Изображение 3">
        </div>
    </div>

    <button id="prev">Предыдущее</button>
    <button id="next">Следующее</button>

    <script src="script.js"></script>
  </section>
  <footer>
    <p>© 2023 Киберклуб</p>
  </footer>
  <script>
	document.addEventListener('DOMContentLoaded', function () {
    const carousel = document.querySelector('.carousel');
    const slides = document.querySelectorAll('.carousel-slide');
    const prevButton = document.getElementById('prev');
    const nextButton = document.getElementById('next');

    let currentIndex = 0;

    function showSlide(index) {
        slides.forEach((slide, i) => {
            slide.style.transform = `translateX(${100 * (i - index)}%)`;
        });
    }

    prevButton.addEventListener('click', function () {
        currentIndex = (currentIndex - 1 + slides.length) % slides.length;
        showSlide(currentIndex);
    });

    nextButton.addEventListener('click', function () {
        currentIndex = (currentIndex + 1) % slides.length;
        showSlide(currentIndex);
    });

    showSlide(currentIndex);
});
  </script>
  <header>
    <h1>Киберклуб "Виртуальные Герои"</h1>
    <p>Играйте, соревнуйтесь и побеждайте!</p>
</header>



<section class="tariffs">
    <h2>Тарифные планы</h2>
    <ul>
        <li>
            <h3>Базовый</h3>
            <p>Доступ к основным играм - 500 рублей/месяц</p>
        </li>
        <li>
            <h3>Продвинутый</h3>
            <p>Доступ ко всем играм - 1000 рублей/месяц</p>
        </li>
        <li>
            <h3>Премиум</h3>
            <p>Доступ ко всем играм + VIP-столик - 1500 рублей/месяц</p>
        </li>
    </ul>
</section>

<section class="request-form">
    <h2>Оставьте заявку</h2>
    <form>
        <label for="name">Ваше имя:</label>
        <input type="text" id="name" name="name" required>
        <label for="email">Ваш Email:</label>
        <input type="email" id="email" name="email" required>
        <button type="submit">Отправить</button>
    </form>
</section>

<section class="user-account">
    <h2>Личный кабинет</h2>
    <p>Войдите в свой личный кабинет, чтобы управлять вашим аккаунтом.</p>
    <a href="login.html">Войти</a>
</section>

<footer>
    <p>&copy; 2023 Киберклуб "Виртуальные Герои"</p>
</footer>
<style>
    body {
font-family: Arial, sans-serif;
}

header {
background-image: url('header-background.jpg');
text-align: center;
color: white;
padding: 100px 0;
}

.carousel {
display: flex;
overflow: hidden;
}

.carousel-item {
flex: 0 0 100%;
}

.tariffs {
text-align: center;
}

.tariffs ul {
list-style: none;
padding: 0;
}

.tariffs li {
border: 1px solid #ccc;
padding: 20px;
margin: 10px;
display: inline-block;
width: 30%;
}

.request-form {
text-align: center;
}

.request-form form {
display: inline-block;
}

.user-account {
text-align: center;
margin-top: 50px;
margin-bottom: 100px;
}

footer {
background-color: #333;
color: white;
text-align: center;
padding: 10px 0;
}
</style>
</body>
</html>
