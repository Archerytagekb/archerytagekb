<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Archery Tag Екатеринбург - Лучный бой в реальном времени</title>
    <style>
        /* Основные стили */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: #f8f9fa;
        }

        /* Шапка */
        header {
            background: linear-gradient(rgba(0, 0, 0, 0.8), rgba(0, 0, 0, 0.8)), 
                        url('https://images.unsplash.com/photo-1546519638-68e109498ffc?auto=format&fit=crop&w=1600');
            background-size: cover;
            background-position: center;
            color: white;
            padding: 20px 0;
            position: relative;
        }

        .header-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .logo h1 {
            font-size: 1.8em;
            color: #ff6b35;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
        }

        /* Навигация */
        nav ul {
            display: flex;
            list-style: none;
            gap: 30px;
        }

        nav a {
            color: white;
            text-decoration: none;
            font-weight: bold;
            font-size: 1.1em;
            transition: color 0.3s;
            padding: 5px 10px;
            border-radius: 3px;
        }

        nav a:hover {
            color: #ff6b35;
            background-color: rgba(255, 255, 255, 0.1);
        }

        /* Герой секция */
        .hero {
            text-align: center;
            padding: 100px 20px;
            background: rgba(0, 0, 0, 0.7);
        }

        .hero h2 {
            font-size: 3.5em;
            margin-bottom: 20px;
            color: #ff6b35;
            text-transform: uppercase;
        }

        .hero p {
            font-size: 1.3em;
            margin-bottom: 30px;
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
        }

        .cta-button {
            display: inline-block;
            background-color: #ff6b35;
            color: white;
            padding: 15px 40px;
            border-radius: 30px;
            text-decoration: none;
            font-size: 1.2em;
            font-weight: bold;
            transition: all 0.3s;
            border: 3px solid #ff6b35;
        }

        .cta-button:hover {
            background-color: transparent;
            transform: scale(1.05);
        }

        /* Секции */
        .section {
            padding: 80px 20px;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            text-align: center;
            font-size: 2.5em;
            color: #2c3e50;
            margin-bottom: 50px;
            position: relative;
        }

        .section-title:after {
            content: '';
            display: block;
            width: 100px;
            height: 4px;
            background-color: #ff6b35;
            margin: 15px auto;
        }

        /* О нас */
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
        }

        .about-image {
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
        }

        .about-image img {
            width: 100%;
            height: auto;
            display: block;
        }

        /* Особенности */
        .features {
            background-color: #2c3e50;
            color: white;
        }

        .features .section-title {
            color: white;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .feature-card {
            background-color: rgba(255, 255, 255, 0.1);
            padding: 30px;
            border-radius: 10px;
            text-align: center;
            transition: transform 0.3s;
        }

        .feature-card:hover {
            transform: translateY(-10px);
        }

        .feature-icon {
            font-size: 3em;
            color: #ff6b35;
            margin-bottom: 20px;
        }

        /* Цены */
        .pricing-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .price-card {
            background: white;
            border-radius: 10px;
            padding: 40px 30px;
            text-align: center;
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
            border: 2px solid #e0e0e0;
            transition: all 0.3s;
        }

        .price-card:hover {
            border-color: #ff6b35;
            transform: translateY(-10px);
        }

        .price-card.popular {
            border-color: #ff6b35;
            position: relative;
        }

        .popular-tag {
            position: absolute;
            top: -15px;
            left: 50%;
            transform: translateX(-50%);
            background-color: #ff6b35;
            color: white;
            padding: 5px 15px;
            border-radius: 20px;
            font-size: 0.9em;
        }

        .price {
            font-size: 2.5em;
            color: #ff6b35;
            font-weight: bold;
            margin: 20px 0;
        }

        .price-period {
            color: #666;
            font-size: 0.9em;
        }

        /* Галерея */
        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
        }

        .gallery-item {
            border-radius: 10px;
            overflow: hidden;
            position: relative;
            cursor: pointer;
        }

        .gallery-item img {
            width: 100%;
            height: 200px;
            object-fit: cover;
            transition: transform 0.3s;
        }

        .gallery-item:hover img {
            transform: scale(1.1);
        }

        /* Контакты */
        .contact-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
        }

        .contact-form input,
        .contact-form textarea {
            width: 100%;
            padding: 15px;
            margin-bottom: 20px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1em;
        }

        .contact-form textarea {
            height: 150px;
            resize: vertical;
        }

        .contact-info {
            padding: 30px;
            background-color: #f8f9fa;
            border-radius: 10px;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 15px;
            margin-bottom: 20px;
        }

        /* Футер */
        footer {
            background-color: #2c3e50;
            color: white;
            padding: 50px 20px 20px;
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
        }

        .copyright {
            text-align: center;
            margin-top: 40px;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }

        /* Модальное окно */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.8);
            z-index: 1000;
            justify-content: center;
            align-items: center;
        }

        .modal-content {
            background: white;
            padding: 40px;
            border-radius: 10px;
            max-width: 500px;
            width: 90%;
            position: relative;
        }

        .close-modal {
            position: absolute;
            top: 15px;
            right: 15px;
            font-size: 1.5em;
            cursor: pointer;
            color: #666;
        }

        /* Адаптивность */
        @media (max-width: 768px) {
            .header-container {
                flex-direction: column;
                gap: 20px;
            }

            nav ul {
                flex-wrap: wrap;
                justify-content: center;
            }

            .hero h2 {
                font-size: 2.5em;
            }

            .about-content,
            .contact-content {
                grid-template-columns: 1fr;
            }

            .gallery-grid {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        @media (max-width: 480px) {
            .hero h2 {
                font-size: 2em;
            }

            .section {
                padding: 50px 20px;
            }

            .section-title {
                font-size: 2em;
            }

            .gallery-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Шапка -->
    <header>
        <div class="header-container">
            <div class="logo">
                <h1>Archery Tag Екатеринбург</h1>
            </div>
            <nav>
                <ul>
                    <li><a href="#home">Главная</a></li>
                    <li><a href="#about">О игре</a></li>
                    <li><a href="#features">Преимущества</a></li>
                    <li><a href="#pricing">Цены</a></li>
                    <li><a href="#gallery">Галерея</a></li>
                    <li><a href="#contact">Забронировать</a></li>
                </ul>
            </nav>
        </div>
        
        <!-- Герой секция -->
        <section class="hero" id="home">
            <div class="container">
                <h2>Лучный бой в Екатеринбурге</h2>
                <p>Адреналин, стратегия и незабываемые эмоции! Archery Tag - это безопасный и экстремальный вид спорта, сочетающий в себе лучную стрельбу и тактические командные бои.</p>
                <a href="#contact" class="cta-button">Забронировать игру</a>
            </div>
        </section>
    </header>

    <!-- О игре -->
    <section class="section" id="about">
        <div class="container">
            <h2 class="section-title">Что такое Archery Tag?</h2>
            <div class="about-content">
                <div class="about-image">
                    <!-- Замените на реальное изображение -->
                    <img src="https://images.unsplash.com/photo-1547036967-23a11d4bd0b7?auto=format&fit=crop&w=800" alt="Archery Tag игра">
                </div>
                <div>
                    <h3 style="font-size: 1.8em; margin-bottom: 20px; color: #2c3e50;">Экстремальный командный бой</h3>
                    <p style="margin-bottom: 15px; font-size: 1.1em;">Archery Tag - это динамичная спортивная игра, сочетающая в себе элементы лучного боя, тактики и стратегии. Участники используют безопасные луки и мягкие стрелы с поролоновыми наконечниками.</p>
                    <p style="margin-bottom: 15px; font-size: 1.1em;">Игра проходит на специальной площадке с укрытиями, где команды сражаются друг против друга. Цель - поразить всех игроков противника или захватить флаг.</p>
                    <p style="margin-bottom: 15px; font-size: 1.1em;"><strong>Безопасность:</strong> Все оборудование сертифицировано и абсолютно безопасно. Мы предоставляем полную экипировку и проводим обязательный инструктаж.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Преимущества -->
    <section class="section features" id="features">
        <div class="container">
            <h2 class="section-title">Почему выбирают нас?</h2>
            <div class="features-grid">
                <div class="feature-card">
                    <div class="feature-icon">🎯</div>
                    <h3>Профессиональное оборудование</h3>
                    <p>Современные безопасные луки и стрелы с поролоновыми наконечниками</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">🛡️</div>
                    <h3>Полная безопасность</h3>
                    <p>Сертифицированная экипировка, инструктаж и контроль на протяжении всей игры</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">🏆</div>
                    <h3>Опытные инструкторы</h3>
                    <p>Профессиональные тренеры с многолетним опытом проведения игр</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">📍</div>
                    <h3>Удобное расположение</h3>
                    <p>Площадка в центре Екатеринбурга с удобной транспортной доступностью</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">🎉</div>
                    <h3>Идеально для мероприятий</h3>
                    <p>Корпоративы, дни рождения, мальчишники и тимбилдинги</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">📸</div>
                    <h3>Фото и видео съемка</h3>
                    <p>Профессиональная съемка вашей игры на память</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Цены -->
    <section class="section" id="pricing">
        <div class="container">
            <h2 class="section-title">Наши тарифы</h2>
            <div class="pricing-grid">
                <div class="price-card">
                    <h3>Разовое посещение</h3>
                    <div class="price">1 200 ₽</div>
                    <p class="price-period">за человека</p>
                    <ul style="text-align: left; margin: 20px 0; list-style: none;">
                        <li style="margin-bottom: 10px; padding-left: 25px; position: relative;">✓ 1.5 часа игры</li>
                        <li style="margin-bottom: 10px; padding-left: 25px; position: relative;">✓ Полная экипировка</li>
                        <li style="margin-bottom: 10px; padding-left: 25px; position: relative;">✓ Инструктаж</li>
                        <li style="margin-bottom: 10px; padding-left: 25px; position: relative;">✓ 3 сценария игры</li>
                    </ul>
                    <a href="#contact" class="cta-button" style="padding: 12px 30px; font-size: 1em;">Выбрать</a>
                </div>
                
                <div class="price-card popular">
                    <div class="popular-tag">Популярно</div>
                    <h3>Командный пакет</h3>
                    <div class="price">8 000 ₽</div>
                    <p class="price-period">до 10 человек</p>
                    <ul style="text-align: left; margin: 20px 0; list-style: none;">
                        <li style="margin-bottom: 10px; padding-left: 25px; position: relative;">✓ 2 часа игры</li>
                        <li style="margin-bottom: 10px; padding-left: 25px; position: relative;">✓ Фотосъемка</li>
                        <li style="margin-bottom: 10px; padding-left: 25px; position: relative;">✓ 5 сценариев игры</li>
                        <li style="margin-bottom: 10px; padding-left: 25px; position: relative;">✓ Комната отдыха</li>
                    </ul>
                    <a href="#contact" class="cta-button" style="padding: 12px 30px; font-size: 1em;">Выбрать</a>
                </div>
                
                <div class="price-card">
                    <h3>Корпоративный</h3>
                    <div class="price">15 000 ₽</div>
                    <p class="price-period">до 20 человек</p>
                    <ul style="text-align: left; margin: 20px 0; list-style: none;">
                        <li style="margin-bottom: 10px; padding-left: 25px; position: relative;">✓ 3 часа игры</li>
                        <li style="margin-bottom: 10px; padding-left: 25px; position: relative;">✓ Видеосъемка</li>
                        <li style="margin-bottom: 10px; padding-left: 25px; position: relative;">✓ Все сценарии</li>
                        <li style="margin-bottom: 10px; padding-left: 25px; position: relative;">✓ Кейтеринг</li>
                    </ul>
                    <a href="#contact" class="cta-button" style="padding: 12px 30px; font-size: 1em;">Выбрать</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Галерея -->
    <section class="section" id="gallery">
        <div class="container">
            <h2 class="section-title">Наша площадка</h2>
            <div class="gallery-grid">
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1547036967-23a11d4bd0b7?auto=format&fit=crop&w=600" alt="Игровая площадка">
                </div>
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1546519638-68e109498ffc?auto=format&fit=crop&w-600" alt="Луки и стрелы">
                </div>
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1518611012118-696072aa579a?auto=format&fit=crop&w=600" alt="Командная игра">
                </div>
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1571019613454-1cb2f99b2d8b?auto=format&fit=crop&w=600" alt="Инструктаж">
                </div>
            </div>
        </div>
    </section>

    <!-- Контакты -->
    <section class="section" id="contact">
        <div class="container">
            <h2 class="section-title">Забронировать игру</h2>
            <div class="contact-content">
                <div>
                    <h3 style="font-size: 1.8em; margin-bottom: 30px; color: #2c3e50;">Оставьте заявку</h3>
                    <form class="contact-form" id="bookingForm">
                        <input type="text" placeholder="Ваше имя" required>
                        <input type="tel" placeholder="Телефон" required>
                        <input type="email" placeholder="Email">
                        <input type="number" placeholder="Количество человек" min="2" max="50" required>
                        <input type="date" required>
                        <textarea placeholder="Дополнительная информация"></textarea>
                        <button type="submit" class="cta-button" style="width: 100%; padding: 15px; font-size: 1.1em;">Отправить заявку</button>
                    </form>
                </div>
                <div class="contact-info">
                    <h3 style="font-size: 1.8em; margin-bottom: 30px; color: #2c3e50;">Контакты</h3>
                    <div class="contact-item">
                        <span style="font-size: 1.5em;">📍</span>
                        <div>
                            <strong>Адрес:</strong><br>
                            г. Екатеринбург, ул. Ленина, 50 (ТРЦ "Гринвич")
                        </div>
                    </div>
                    <div class="contact-item">
                        <span style="font-size: 1.5em;">📞</span>
                        <div>
                            <strong>Телефон:</strong><br>
                            +7 (343) 123-45-67
                        </div>
                    </div>
                    <div class="contact-item">
                        <span style="font-size: 1.5em;">🕒</span>
                        <div>
                            <strong>Часы работы:</strong><br>
                            Ежедневно с 10:00 до 22:00
                        </div>
                    </div>
                    <div class="contact-item">
                        <span style="font-size: 1.5em;">✉️</span>
                        <div>
                            <strong>Email:</strong><br>
                            info@archerytag-ekb.ru
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Футер -->
    <footer>
        <div class="footer-content">
            <div>
                <h3>Archery Tag Екатеринбург</h3>
                <p style="margin-top: 15px;">Лучший способ провести время с друзьями или коллегами. Адреналин, стратегия и незабываемые эмоции!</p>
            </div>
            <div>
                <h3>Быстрые ссылки</h3>
                <ul style="list-style: none; margin-top: 15px;">
                    <li style="margin-bottom: 10px;"><a href="#home" style="color: #ccc; text-decoration: none;">Главная</a></li>
                    <li style="margin-bottom: 10px;"><a href="#about" style="color: #ccc; text-decoration: none;">О игре</a></li>
                    <li style="margin-bottom: 10px;"><a href="#pricing" style="color: #ccc; text-decoration: none;">Цены</a></li>
                    <li style="margin-bottom: 10px;"><a href="#contact" style="color: #ccc; text-decoration: none;">Контакты</a></li>
                </ul>
            </div>
            <div>
                <h3>Мы в соцсетях</h3>
                <p style="margin-top: 15px; color: #ccc;">Следите за нами в социальных сетях, чтобы быть в курсе акций и мероприятий</p>
                <div style="display: flex; gap: 15px; margin-top: 15px; font-size: 1.5em;">
                    <span>📱</span>
                    <span>📷</span>
                    <span>🎥</span>
                </div>
            </div>
        </div>
        <div class="copyright">
            <p>&copy; 2024 Archery Tag Екатеринбург. Все права защищены.</p>
        </div>
    </footer>

    <!-- Модальное окно подтверждения -->
    <div class="modal" id="successModal">
        <div class="modal-content">
            <span class="close-modal" onclick="closeModal()">×</span>
            <h2 style="color: #2c3e50; margin-bottom: 20px;">Заявка отправлена!</h2>
            <p>Мы свяжемся с вами в течение 30 минут для подтверждения бронирования.</p>
            <p style="margin-top: 20px; font-size: 0.9em; color: #666;">Спасибо, что выбрали Archery Tag!</p>
        </div>
    </div>

    <script>
        // Плавная прокрутка
        document.querySelectorAll('nav a').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                const targetId = this.getAttribute('href');
                const targetElement = document.querySelector(targetId);
                if (targetElement) {
                    targetElement.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Обработка формы
        document.getElementById('bookingForm').addEventListener('submit', function(e) {
            e.preventDefault();
            document.getElementById('successModal').style.display = 'flex';
        });

        // Закрытие модального окна
        function closeModal() {
            document.getElementById('successModal').style.display = 'none';
        }

        // Закрытие по клику вне окна
        window.onclick = function(event) {
            const modal = document.getElementById('successModal');
            if (event.target === modal) {
                closeModal();
            }
        }

        // Валидация даты (нельзя выбрать прошедшие даты)
        const dateInput = document.querySelector('input[type="date"]');
        const today = new Date().toISOString().split('T')[0];
        dateInput.min = today;

        // Анимация при скролле
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);

        // Наблюдаем за карточками
        document.querySelectorAll('.feature-card, .price-card').forEach(card => {
            card.style.opacity = '0';
            card.style.transform = 'translateY(20px)';
            card.style.transition = 'opacity 0.5s, transform 0.5s';
            observer.observe(card);
        });
    </script>
</body>
</html>
