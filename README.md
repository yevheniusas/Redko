<!DOCTYPE html>
<html lang="uk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TAXI Світязь | Швидкі Трансфери у Шацьку 24/7</title>
    <!-- Підключення Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        // Конфігурація Tailwind, визначаємо кастомні кольори та активуємо темний режим через клас
        tailwind.config = {
            darkMode: 'class', // Активація темного режиму через клас 'dark' на <body>
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                    },
                    colors: {
                        // Темна палітра
                        'primary-dark': '#0f172a', // Дуже темний фон (для темної теми)
                        'secondary-dark': '#1e293b', // Фон карток (для темної теми)
                        'accent-gold': '#ffd700', // Золотистий акцент
                        'accent-white': '#f3f4f6', // Світлий текст (для темної теми)
                        'operator-bg': '#374151', // Сірий фон для оператора (для темної теми)
                        
                        // Світла палітра (буде використовуватися за замовчуванням)
                        'light-bg': '#f9fafb', // Дуже світлий фон
                        'light-card': '#ffffff', // Фон карток
                        'light-text': '#1f2937', // Темний текст
                    }
                }
            }
        }
    </script>
    <style>
        /* Стилі, що не залежать від теми */
        body {
            font-family: 'Inter', sans-serif;
            min-height: 100vh;
            transition: background-color 0.3s, color 0.3s; /* Плавний перехід кольорів */
        }
        .hero-section {
            padding-top: 4rem; 
            padding-bottom: 4rem;
        }
        .cta-button {
            transition: background-color 0.3s ease;
            /* Тінь залишаємо золотистою для обох тем */
            box-shadow: 0 4px 15px rgba(255, 215, 0, 0.3);
        }
        .cta-button:hover {
            box-shadow: 0 6px 20px rgba(255, 215, 0, 0.5);
        }
        /* Font Awesome залишаємо для інших іконок */
        @import url('https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css');
        
        @media (min-width: 640px) {
             .hero-section {
                padding-top: 8rem; 
                padding-bottom: 8rem;
            }
        }
    </style>
</head>
<!-- Основні класи: за замовчуванням - світла тема, з класом 'dark' - темна тема -->
<body class="flex flex-col items-center justify-start bg-light-bg text-light-text dark:bg-primary-dark dark:text-accent-white">

    <!-- Верхнє Меню (як у прикладі: лого/назва та кнопка) -->
    <nav class="w-full bg-light-card shadow-lg dark:bg-primary-dark dark:shadow-2xl px-4 sm:px-8 py-3 sm:py-4 flex justify-between items-center fixed top-0 z-20">
        <span class="text-lg sm:text-xl font-bold text-light-text dark:text-accent-white">TAXI Світязь</span>
        <div class="flex items-center">
            <!-- Кнопка Перемикання Теми (Збільшений розмір: p-3) -->
            <button id="theme-toggle" class="p-3 mr-3 sm:mr-4 rounded-full bg-gray-300 hover:bg-gray-400 dark:bg-gray-700 dark:hover:bg-gray-600 text-gray-900 dark:text-accent-white transition duration-200" aria-label="Перемкнути тему">
                <!-- Контейнер для анімації переходу між іконками. Розмір 1.5rem (w-6 h-6) -->
                <span id="theme-icon-wrapper" class="relative w-6 h-6 flex items-center justify-center">
                    
                    <!-- 1. Іконка Місяця (Custom SVG, викликає перехід до Темної теми) - ФІНАЛЬНА НАДІЙНА ВЕРСІЯ -->
                    <svg id="moon-icon" class="w-full h-full absolute transition-opacity duration-300" fill="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                        <path d="M12 21a9 9 0 0 0 8.017-4.832 9 9 0 0 1-13.435-13.435A9 9 0 0 0 12 21z"/>
                    </svg>

                    <!-- 2. Іконка Сонця (Custom SVG, викликає перехід до Світлої теми) - НАДІЙНИЙ ВАРІАНТ -->
                    <svg id="sun-icon" class="w-full h-full absolute transition-opacity duration-300" fill="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                        <!-- Коло і промені -->
                        <circle cx="12" cy="12" r="5" stroke="currentColor" stroke-width="2" fill="none"/>
                        <path d="M12 2v2m0 18v-2M4.22 4.22l1.42 1.42M18.36 18.36l1.42 1.42M2 12h2m18 0h-2M4.22 19.78l1.42-1.42M18.36 5.64l1.42-1.42" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
                    </svg>
                </span>
            </button>

            <!-- Кнопка Викликати -->
            <a href="tel:+380777702202" class="bg-gray-700 hover:bg-gray-600 text-accent-white font-medium py-1.5 px-3 sm:py-2 sm:px-4 rounded transition duration-200 flex items-center text-sm sm:text-base">
                 <i class="fas fa-phone mr-1 sm:mr-2"></i> Викликати
            </a>
        </div>
    </nav>
    
    <!-- Секція Героя -->
    <!-- ЗАБЕЗПЕЧЕНО: Достатній відступ для фіксованої шапки -->
    <header class="w-full text-center hero-section bg-light-card dark:bg-primary-dark pt-32 sm:pt-28">
        <div class="max-w-3xl mx-auto px-4">
            <!-- Основна назва -->
            <h1 class="text-4xl sm:text-7xl font-extrabold mb-3 sm:mb-4 tracking-wider leading-tight text-light-text dark:text-accent-white">
                Таксі <span class="text-accent-gold">Світязь</span>
            </h1>
            <p class="text-lg sm:text-2xl font-light mb-6 sm:mb-8 text-gray-500 dark:text-gray-400">
                Ваш комфортний та надійний трансфер на Шацьких озерах 24/7.
            </p>

            <!-- КОНТЕЙНЕР ДЛЯ КНОПОК З ВЕРТИКАЛЬНИМ ПРОБІЛОМ (space-y-4) -->
            <div class="flex flex-col items-center space-y-4 sm:space-y-6 cta-button-container">
                
                <!-- Блок 1: Кнопка + Оператор Lifecell -->
                <div class="flex items-stretch justify-center w-full max-w-md">
                    <a href="tel:+380777702202" class="flex-grow cta-button bg-accent-gold hover:bg-yellow-400 text-light-text dark:text-primary-dark font-extrabold py-3 px-4 sm:py-4 sm:px-8 rounded-l-lg rounded-r-none text-lg sm:text-2xl shadow-xl text-left">
                        Замовити: <span class="whitespace-nowrap">+380 77 770 2202</span>
                    </a>
                    <span class="bg-gray-300 dark:bg-operator-bg text-light-text dark:text-accent-white font-medium py-3 px-4 sm:py-4 sm:px-4 rounded-r-lg rounded-l-none text-sm sm:text-lg shadow-xl flex items-center justify-center min-w-[90px] sm:min-w-[120px]">
                        Lifecell
                    </span>
                </div>
                
                <!-- Блок 2: Кнопка + Оператор Vodafone -->
                <div class="flex items-stretch justify-center w-full max-w-md">
                    <a href="tel:+380666602202" class="flex-grow cta-button bg-accent-gold hover:bg-yellow-400 text-light-text dark:text-primary-dark font-extrabold py-3 px-4 sm:py-4 sm:px-8 rounded-l-lg rounded-r-none text-lg sm:text-2xl shadow-xl text-left">
                        Замовити: <span class="whitespace-nowrap">+380 66 660 2202</span>
                    </a>
                    <span class="bg-gray-300 dark:bg-operator-bg text-light-text dark:text-accent-white font-medium py-3 px-4 sm:py-4 sm:px-4 rounded-r-lg rounded-l-none text-sm sm:text-lg shadow-xl flex items-center justify-center min-w-[90px] sm:min-w-[120px]">
                        Vodafone
                    </span>
                </div>

                <!-- Блок 3: Кнопка + Оператор Kyivstar -->
                <div class="flex items-stretch justify-center w-full max-w-md">
                    <a href="tel:+380977702202" class="flex-grow cta-button bg-accent-gold hover:bg-yellow-400 text-light-text dark:text-primary-dark font-extrabold py-3 px-4 sm:py-4 sm:px-8 rounded-l-lg rounded-r-none text-lg sm:text-2xl shadow-xl text-left">
                        Замовити: <span class="whitespace-nowrap">+380 97 770 2202</span>
                    </a>
                    <span class="bg-gray-300 dark:bg-operator-bg text-light-text dark:text-accent-white font-medium py-3 px-4 sm:py-4 sm:px-4 rounded-r-lg rounded-l-none text-sm sm:text-lg shadow-xl flex items-center justify-center min-w-[90px] sm:min-w-[120px]">
                        Kyivstar
                    </span>
                </div>

            </div> 
            <!-- КІНЕЦЬ КОНТЕЙНЕРА -->

        </div>
    </header>

    <!-- Секція Переваги (як у прикладі з трьома картками) -->
    <main class="w-full max-w-4xl p-4 sm:p-10 mt-[-20px] sm:-mt-10 relative z-10">
        <!-- ТЕМНИЙ ТЕКСТ НА ТЕМНОМУ ФОНІ (Згідно з запитом) -->
        <h2 class="text-2xl sm:text-3xl font-bold text-center mb-8 sm:mb-10 text-light-text dark:text-light-text">
            Переваги поїздки з нами
        </h2>

        <div class="grid grid-cols-1 md:grid-cols-3 gap-4 sm:gap-6">
            
            <!-- Картка 1: Комфорт та Надійність -->
            <div class="p-5 sm:p-6 bg-light-card dark:bg-secondary-dark rounded-xl shadow-2xl border border-gray-300 dark:border-gray-700">
                <div class="text-3xl sm:text-4xl text-accent-gold mb-3 sm:mb-4"><i class="fas fa-car"></i></div>
                <h3 class="text-lg sm:text-xl font-bold mb-2 text-light-text dark:text-accent-white">Комфорт та Надійність</h3>
                <p class="text-gray-600 dark:text-gray-400 text-xs sm:text-sm">
                    Тільки чисті автомобілі з клімат-контролем. Забудете про літню спеку та нерівності доріг.
                </p>
            </div>

            <!-- Картка 2: Місцеві Водії -->
            <div class="p-5 sm:p-6 bg-light-card dark:bg-secondary-dark rounded-xl shadow-2xl border border-gray-300 dark:border-gray-700">
                <div class="text-3xl sm:text-4xl text-accent-gold mb-3 sm:mb-4"><i class="fas fa-map-marked-alt"></i></div>
                <h3 class="text-lg sm:text-xl font-bold mb-2 text-light-text dark:text-accent-white">Місцеві Водії</h3>
                <p class="text-gray-600 dark:text-gray-400 text-xs sm:text-sm">
                    Наші водії добре знають Шацький район, тому ми гарантуємо найшвидші маршрути.
                </p>
            </div>

            <!-- Картка 3: Безпека та Прозорість -->
            <div class="p-5 sm:p-6 bg-light-card dark:bg-secondary-dark rounded-xl shadow-2xl border border-gray-300 dark:border-gray-700">
                <div class="text-3xl sm:text-4xl text-accent-gold mb-3 sm:mb-4"><i class="fas fa-shield-alt"></i></div>
                <h3 class="text-lg sm:text-xl font-bold mb-2 text-light-text dark:text-accent-white">Безпека та Прозорість</h3>
                <p class="text-gray-600 dark:text-gray-400 text-xs sm:text-sm">
                    Фіксовані тарифи. Жодних несподіваних доплат. Ваша безпека — наш пріоритет.
                </p>
            </div>
        </div>
    </main>

    <!-- Секція Послуг та Маршрутів -->
    <div class="w-full max-w-4xl p-4 sm:p-10 mt-4 sm:mt-8">
           <!-- ТЕМНИЙ ТЕКСТ НА ТЕМНОМУ ФОНІ (Згідно з запитом) -->
           <h2 class="text-2xl sm:text-3xl font-bold text-center mb-8 sm:mb-10 text-light-text dark:text-light-text">
            Наші основні трансфери
        </h2>
        
        <div class="grid grid-cols-1 md:grid-cols-3 gap-4 sm:gap-6 text-center">
            
            <!-- Послуга 1: Вокзали та міста -->
            <div class="p-5 sm:p-6 bg-light-card dark:bg-secondary-dark rounded-xl shadow-md border border-gray-300 dark:border-gray-700">
                <span class="text-4xl sm:text-5xl text-accent-gold block mb-3">🚉</span>
                <p class="font-semibold text-lg sm:text-xl text-light-text dark:text-accent-white">Вокзали та Міста</p>
                <p class="text-xs sm:text-sm text-gray-600 dark:text-gray-400 mt-1">Ковель, Луцьк, Рівне та інші міста України.</p>
            </div>

            <!-- Послуга 2: Шацькі Озера -->
            <div class="p-5 sm:p-6 bg-light-card dark:bg-secondary-dark rounded-xl shadow-md border border-gray-300 dark:border-gray-700">
                <span class="text-4xl sm:text-5xl text-accent-gold block mb-3">🏞️</span>
                <p class="font-semibold text-lg sm:text-xl text-light-text dark:text-accent-white">Між озерами</p>
                <p class="text-xs sm:text-sm text-gray-600 dark:text-gray-400 mt-1">Світязь, Пульмо, Пісочне, Гряда, Мельники.</p>
            </div>

            <!-- Послуга 3: Поїздки по району -->
            <div class="p-5 sm:p-6 bg-light-card dark:bg-secondary-dark rounded-xl shadow-md border border-gray-300 dark:border-gray-700">
                <span class="text-4xl sm:text-5xl text-accent-gold block mb-3">📍</span>
                <p class="font-semibold text-lg sm:text-xl text-light-text dark:text-accent-white">Поїздки по району</p>
                <p class="text-xs sm:text-sm text-gray-600 dark:text-gray-400 mt-1">Доставка до садиб та приватних адрес.</p>
            </div>
        </div>
    </div>


    <!-- Футер -->
    <footer class="w-full bg-gray-200 dark:bg-gray-900 p-4 sm:p-6 text-center mt-12 sm:mt-16">
        <p class="text-xs sm:text-sm text-gray-500">
            &copy; 2025 TAXI СВІТЯЗЬ. Всі права захищені. | Телефон для замовлень: <a href="tel:+380666602202" class="text-accent-gold hover:underline">(066) 660-22-02</a>
        </p>
    </footer>

    <script>
        // JS для керування темою
        document.addEventListener('DOMContentLoaded', () => {
            const toggle = document.getElementById('theme-toggle');
            const body = document.body;
            const moonIcon = document.getElementById('moon-icon');
            const sunIcon = document.getElementById('sun-icon');

            // Перевіряємо збережені налаштування або налаштування системи
            const prefersDark = window.matchMedia('(prefers-color-scheme: dark)').matches;
            let currentTheme = localStorage.getItem('theme');

            if (!currentTheme) {
                currentTheme = prefersDark ? 'dark' : 'light';
            }

            function applyTheme(theme) {
                // Використовуємо класи opacity для плавного переходу
                if (theme === 'dark') {
                    body.classList.add('dark');
                    // Темна тема: показуємо Сонце (заклик до Світлої теми)
                    moonIcon.classList.remove('opacity-100');
                    moonIcon.classList.add('opacity-0');
                    sunIcon.classList.remove('opacity-0');
                    sunIcon.classList.add('opacity-100');
                } else {
                    body.classList.remove('dark');
                    // Світла тема: показуємо Місяць (заклик до Темної теми)
                    moonIcon.classList.remove('opacity-0');
                    moonIcon.classList.add('opacity-100');
                    sunIcon.classList.remove('opacity-100');
                    sunIcon.classList.add('opacity-0');
                }
                localStorage.setItem('theme', theme);
            }

            // Ініціалізація початкових класів
            // Це потрібно, щоб при першому завантаженні був правильний стан без анімації
            if (currentTheme === 'dark') {
                moonIcon.classList.add('opacity-0');
                sunIcon.classList.add('opacity-100');
            } else {
                moonIcon.classList.add('opacity-100');
                sunIcon.classList.add('opacity-0');
            }
            applyTheme(currentTheme);

            // Обробник натискання кнопки
            toggle.addEventListener('click', () => {
                const newTheme = body.classList.contains('dark') ? 'light' : 'dark';
                applyTheme(newTheme);
            });
        });
    </script>

</body>
</html>
