<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Portootfolio Lola Nadira Syafah</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        :root {
            --bg: #fcf8ff;
            --bg-soft: #f3e8ff;
            --card: #ffffff;
            --primary: #9b70d1;
            --primary-dark: #7547a8;
            --primary-light: #dbc5f3;
            --pink: #f6d4e8;
            --blue: #d5e3fa;
            --text: #3e3448;
            --text-light: #766a80;
            --border: #eadcf5;
            --shadow: 0 10px 30px rgba(120, 78, 155, 0.12);
        }

        body.dark-mode {
            --bg: #211b29;
            --bg-soft: #2d2437;
            --card: #342b3f;
            --primary: #c29ae8;
            --primary-dark: #d8b7f1;
            --primary-light: #644c78;
            --pink: #714e68;
            --blue: #4d5e7d;
            --text: #f7effc;
            --text-light: #c7bdcc;
            --border: #4b3d56;
            --shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }

        body {
            font-family: "Segoe UI", Arial, sans-serif;
            background: var(--bg);
            color: var(--text);
            line-height: 1.7;
            transition: 0.3s;
        }

        a {
            text-decoration: none;
            color: inherit;
        }

        button,
        input {
            font-family: inherit;
        }

        /* NAVBAR */

        .header {
            position: sticky;
            top: 0;
            z-index: 1000;
            background: var(--card);
            border-bottom: 1px solid var(--border);
        }

        .navbar {
            max-width: 1100px;
            min-height: 70px;
            margin: auto;
            padding: 0 25px;

            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .logo {
            font-size: 25px;
            font-weight: 800;
            color: var(--primary-dark);
        }

        .logo span {
            color: #d889bb;
        }

        .nav-menu {
            display: flex;
            gap: 30px;
            list-style: none;
        }

        .nav-menu a {
            color: var(--text-light);
            font-weight: 600;
        }

        .nav-menu a:hover {
            color: var(--primary);
        }

        .menu-toggle,
        .theme-toggle {
            width: 42px;
            height: 42px;
            border: none;
            border-radius: 50%;
            background: var(--bg-soft);
            color: var(--text);
            cursor: pointer;
            font-size: 18px;
        }

        .menu-toggle {
            display: none;
        }

        /* HERO */

        .hero {
            min-height: 650px;
            max-width: 1100px;
            margin: auto;
            padding: 100px 25px;

            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;

            position: relative;
        }

        .hero-content {
            max-width: 760px;
        }

        .hello {
            color: var(--primary);
            font-weight: bold;
            margin-bottom: 15px;
        }

        .hero h1 {
            font-size: clamp(40px, 7vw, 70px);
            line-height: 1.15;
            margin-bottom: 25px;
        }

        .hero h1 span {
            color: var(--primary);
        }

        .hero-description {
            color: var(--text-light);
            font-size: 17px;
        }

        .hero-buttons {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-top: 35px;
        }

        .button {
            display: inline-block;
            padding: 12px 22px;
            border-radius: 50px;
            font-weight: bold;
        }

        .primary-button {
            background: var(--primary);
            color: white;
        }

        .secondary-button {
            border: 2px solid var(--primary-light);
            color: var(--primary-dark);
        }

        .star {
            position: absolute;
            color: var(--primary);
            font-size: 30px;
            animation: floating 3s infinite ease-in-out;
        }

        .star-one {
            top: 130px;
            left: 12%;
        }

        .star-two {
            right: 12%;
            top: 180px;
        }

        .star-three {
            bottom: 100px;
            left: 20%;
        }

        @keyframes floating {
            0%, 100% {
                transform: translateY(0);
            }

            50% {
                transform: translateY(-10px);
            }
        }

        /* SECTION */

        .section {
            max-width: 1100px;
            margin: auto;
            padding: 90px 25px;
        }

        .section-title {
            text-align: center;
            margin-bottom: 50px;
        }

        .section-title p {
            color: var(--primary);
            font-weight: bold;
        }

        .section-title h2 {
            font-size: 38px;
        }

        .section-title span {
            color: var(--text-light);
        }

        /* ABOUT */

        .about-container {
            display: grid;
            grid-template-columns: 350px 1fr;
            gap: 60px;
            align-items: center;
        }

        .profile-card {
            background: var(--card);
            border: 1px solid var(--border);
            padding: 25px;
            border-radius: 30px;
            box-shadow: var(--shadow);
            text-align: center;
        }

        .photo-container {
            width: 230px;
            height: 230px;
            margin: auto auto 20px;
            padding: 8px;
            border-radius: 50%;
            background: var(--bg-soft);
            border: 4px solid var(--primary-light);
            overflow: hidden;
        }

        .profile-photo {
            width: 100%;
            height: 100%;
            object-fit: cover;
            border-radius: 50%;
        }

        .profile-name h3 {
            color: var(--primary-dark);
        }

        .profile-name p,
        .about-text p {
            color: var(--text-light);
        }

        .education {
            display: grid;
            gap: 12px;
            margin-top: 25px;
        }

        .education-item {
            display: flex;
            align-items: center;
            gap: 15px;
            padding: 14px;
            background: var(--bg-soft);
            border-radius: 18px;
        }

        .education-item > span {
            width: 42px;
            height: 42px;
            display: flex;
            align-items: center;
            justify-content: center;
            background: var(--card);
            border-radius: 50%;
        }

        .education-item small {
            color: var(--primary);
            font-weight: bold;
        }

        /* PROJECT */

        .projects-section {
            max-width: none;
            background: var(--bg-soft);
        }

        .project-grid {
            max-width: 1100px;
            margin: auto;

            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 25px;
        }

        .project-card {
            background: var(--card);
            border: 1px solid var(--border);
            border-radius: 25px;
            padding: 25px;
            box-shadow: var(--shadow);
        }

        .project-icon {
            width: 65px;
            height: 65px;

            display: flex;
            align-items: center;
            justify-content: center;

            border-radius: 20px;
            font-size: 30px;
            margin-bottom: 20px;
        }

        .purple-icon {
            background: var(--primary-light);
        }

        .pink-icon {
            background: var(--pink);
        }

        .blue-icon {
            background: var(--blue);
        }

        .project-number {
            color: var(--primary);
            font-size: 13px;
            font-weight: bold;
        }

        .project-content h3 {
            margin: 5px 0 10px;
        }

        .project-content p {
            color: var(--text-light);
            font-size: 14px;
            margin-bottom: 18px;
        }

        .project-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 7px;
            margin-bottom: 20px;
        }

        .project-tags span {
            background: var(--bg-soft);
            color: var(--primary-dark);
            padding: 5px 10px;
            border-radius: 50px;
            font-size: 11px;
            font-weight: bold;
        }

        .demo-button {
            width: 100%;
            border: none;
            padding: 11px;
            border-radius: 15px;
            background: var(--primary);
            color: white;
            cursor: pointer;
            font-weight: bold;
        }

        /* SKILLS */

        .skills-container {
            max-width: 700px;
            margin: auto;
            display: grid;
            gap: 25px;
        }

        .skill-info {
            display: flex;
            justify-content: space-between;
            margin-bottom: 7px;
            font-weight: bold;
        }

        .skill-info span:last-child {
            color: var(--primary);
        }

        .skill-bar {
            height: 10px;
            background: var(--bg-soft);
            border-radius: 20px;
            overflow: hidden;
        }

        .skill-progress {
            height: 100%;
            background: var(--primary);
            border-radius: 20px;
        }

        .html-progress { width: 80%; }
        .css-progress { width: 75%; }
        .js-progress { width: 60%; }
        .ui-progress { width: 70%; }

        /* CONTACT */

        .contact-card {
            max-width: 700px;
            margin: auto;
            padding: 45px 30px;
            background: var(--card);
            border: 1px solid var(--border);
            border-radius: 30px;
            box-shadow: var(--shadow);
            text-align: center;
        }

        .contact-card > p {
            color: var(--text-light);
            margin-bottom: 30px;
        }

        .contact-list {
            display: grid;
            gap: 15px;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 15px;
            text-align: left;
            padding: 15px 20px;
            border-radius: 18px;
            background: var(--bg-soft);
        }

        .contact-item > span:first-child {
            font-size: 25px;
        }

        .contact-item span {
            display: flex;
            flex-direction: column;
        }

        .contact-item small {
            color: var(--primary);
            font-weight: bold;
        }

        /* FOOTER */

        .footer {
            padding: 30px 20px;
            text-align: center;
            background: var(--bg-soft);
            border-top: 1px solid var(--border);
            color: var(--text-light);
            font-size: 13px;
        }

        /* BUTTON SCROLL */

        .scroll-top {
            position: fixed;
            right: 25px;
            bottom: 25px;

            width: 45px;
            height: 45px;

            border: none;
            border-radius: 50%;

            background: var(--primary);
            color: white;

            cursor: pointer;
            font-size: 20px;

            opacity: 0;
            visibility: hidden;
            z-index: 1000;
        }

        .scroll-top.show {
            opacity: 1;
            visibility: visible;
        }

        /* MODAL */

        .modal {
            position: fixed;
            inset: 0;

            background: rgba(20, 15, 25, 0.65);

            display: none;
            align-items: center;
            justify-content: center;

            padding: 20px;
            z-index: 2000;
        }

        .modal.active {
            display: flex;
        }

        .modal-box {
            width: 100%;
            max-width: 500px;

            background: var(--card);

            border-radius: 25px;
            padding: 30px;

            box-shadow: var(--shadow);

            max-height: 90vh;
            overflow-y: auto;
        }

        .modal-box h3 {
            color: var(--primary-dark);
            margin-bottom: 20px;
            text-align: center;
        }

        .close-modal {
            width: 100%;
            border: none;
            padding: 10px;
            margin-top: 20px;
            border-radius: 12px;
            background: var(--primary);
            color: white;
            cursor: pointer;
            font-weight: bold;
        }

        /* KALKULATOR */

        .calculator {
            max-width: 320px;
            margin: auto;
        }

        .calculator-display {
            width: 100%;
            height: 65px;

            border: none;
            border-radius: 15px;

            padding: 10px 15px;

            background: var(--bg-soft);
            color: var(--text);

            text-align: right;
            font-size: 28px;

            margin-bottom: 12px;
        }

        .calculator-buttons {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 8px;
        }

        .calculator-buttons button {
            height: 55px;
            border: none;
            border-radius: 14px;
            background: var(--bg-soft);
            color: var(--text);
            font-size: 18px;
            font-weight: bold;
            cursor: pointer;
        }

        .calculator-buttons button:hover {
            background: var(--primary-light);
        }

        .calculator-buttons .operator {
            background: var(--primary);
            color: white;
        }

        .calculator-buttons .equal {
            background: var(--primary-dark);
            color: white;
        }

        /* JADWAL */

        .form-group {
            display: flex;
            gap: 8px;
            margin-bottom: 15px;
        }

        .form-group input {
            width: 100%;
            padding: 12px;
            border: 1px solid var(--border);
            border-radius: 12px;
            background: var(--bg);
            color: var(--text);
            outline: none;
        }

        .add-button {
            border: none;
            padding: 12px 18px;
            border-radius: 12px;
            background: var(--primary);
            color: white;
            cursor: pointer;
            font-weight: bold;
        }

        .schedule-list {
            display: grid;
            gap: 10px;
        }

        .schedule-item {
            padding: 14px;
            background: var(--bg-soft);
            border-radius: 14px;

            display: flex;
            justify-content: space-between;
            align-items: center;
            gap: 10px;
        }

        .delete-small {
            border: none;
            background: #e99ab9;
            color: white;
            border-radius: 8px;
            padding: 7px 10px;
            cursor: pointer;
        }

        /* TODO */

        .todo-input {
            display: flex;
            gap: 8px;
            margin-bottom: 15px;
        }

        .todo-input input {
            flex: 1;
            padding: 12px;
            border: 1px solid var(--border);
            border-radius: 12px;
            background: var(--bg);
            color: var(--text);
            outline: none;
        }

        .todo-list {
            display: grid;
            gap: 10px;
        }

        .todo-item {
            display: flex;
            align-items: center;
            gap: 10px;

            padding: 12px;

            background: var(--bg-soft);
            border-radius: 14px;
        }

        .todo-item span {
            flex: 1;
        }

        .todo-item.completed span {
            text-decoration: line-through;
            opacity: 0.5;
        }

        .todo-check {
            width: 20px;
            height: 20px;
            cursor: pointer;
        }

        /* MOBILE */

        @media (max-width: 600px) {

            .navbar {
                min-height: 65px;
                padding: 0 18px;
            }

            .logo {
                font-size: 22px;
            }

            .menu-toggle {
                display: block;
                margin-left: auto;
                margin-right: 8px;
            }

            .nav-menu {
                position: absolute;
                top: 65px;
                left: 0;
                right: 0;

                display: none;

                flex-direction: column;
                gap: 0;

                padding: 10px 20px 20px;

                background: var(--card);
                border-bottom: 1px solid var(--border);
            }

            .nav-menu.active {
                display: flex;
            }

            .nav-menu a {
                display: block;
                padding: 12px;
            }

            .hero {
                min-height: 600px;
                padding: 80px 20px;
            }

            .hero h1 {
                font-size: 40px;
            }

            .hero-description {
                font-size: 15px;
            }

            .hero-buttons {
                flex-direction: column;
                align-items: center;
            }

            .button {
                width: 100%;
                max-width: 250px;
                text-align: center;
            }

            .section {
                padding: 70px 20px;
            }

            .section-title h2 {
                font-size: 30px;
            }

            .about-container {
                grid-template-columns: 1fr;
                gap: 35px;
            }

            .photo-container {
                width: 200px;
                height: 200px;
            }

            .project-grid {
                grid-template-columns: 1fr;
            }

            .contact-card {
                padding: 35px 20px;
            }

            .form-group {
                flex-direction: column;
            }

            .todo-input {
                flex-direction: column;
            }
        }

        @media (min-width: 601px) and (max-width: 900px) {

            .project-grid {
                grid-template-columns: repeat(2, 1fr);
            }

            .about-container {
                grid-template-columns: 280px 1fr;
                gap: 30px;
            }
        }
    </style>
</head>

<body>

<header class="header">

    <nav class="navbar">

        <a href="#beranda" class="logo">
            Lola<span>♡</span>
        </a>

        <button
            class="menu-toggle"
            id="menu-toggle"
        >
            ☰
        </button>

        <ul class="nav-menu" id="nav-menu">

            <li><a href="#beranda">Beranda</a></li>
            <li><a href="#tentang">Tentang</a></li>
            <li><a href="#proyek">Proyek</a></li>
            <li><a href="#kontak">Kontak</a></li>

        </ul>

        <button
            class="theme-toggle"
            id="theme-toggle"
        >
            🌙
        </button>

    </nav>

</header>


<main>

    <!-- HERO -->

    <section class="hero" id="beranda">

        <div class="hero-content">

            <p class="hello">♡ Hello, welcome!</p>

            <h1>
                Halo, aku
                <span>Lola Nadira Syafah</span>
                💜
            </h1>

            <p class="hero-description">
                Pelajar kelas X RPL 3 yang sedang belajar
                membuat website dengan HTML, CSS,
                dan JavaScript.
            </p>

            <div class="hero-buttons">

                <a href="#proyek"
                   class="button primary-button">
                    Lihat Proyek ✨
                </a>

                <a href="#kontak"
                   class="button secondary-button">
                    Hubungi Aku
                </a>

            </div>

        </div>

        <div class="star star-one">✦</div>
        <div class="star star-two">♡</div>
        <div class="star star-three">✧</div>

    </section>


    <!-- TENTANG -->

    <section class="section" id="tentang">

        <div class="section-title">

            <p>♡ Get to know me</p>

            <h2>Tentang Saya</h2>

        </div>


        <div class="about-container">

            <div class="profile-card">

                <div class="photo-container">

                    <img
                        src="https://uploads.onecompiler.io/45447qjvv/4544ayvsp/WhatsApp%20Image%202026-09-24%20at%2012.33.57.jpeg"
                        alt=""
                        class="profile-photo"
                    >

                </div>

                <div class="profile-name">

                    <h3>Lola Nadira Syafah</h3>

                    <p>Student • X RPL 3</p>

                </div>

            </div>


            <div class="about-text">

                <p>
                    Hai! Namaku
                    <strong>Lola Nadira Syafah</strong>.
                    Aku adalah siswi kelas
                    <strong>X RPL 3</strong>
                    di SMK Krian 1 Sidoarjo.
                </p>

                <p>
                    Aku sedang belajar pemrograman,
                    desain UI/UX, dan pembuatan website.
                    
                </p>


                <div class="education">

                    <div class="education-item">
                        <span>🎀</span>
                        <div>
                            <small>SD</small>
                            <h4>SDN Seketi</h4>
                        </div>
                    </div>

                    <div class="education-item">
                        <span>🌷</span>
                        <div>
                            <small>SMP</small>
                            <h4>SMP Budi Utomo Prambon</h4>
                        </div>
                    </div>

                    <div class="education-item">
                        <span>💜</span>
                        <div>
                            <small>SMK</small>
                            <h4>SMK Krian 1 Sidoarjo</h4>
                        </div>
                    </div>

                </div>

            </div>

        </div>

    </section>


    <!-- PROYEK -->

    <section class="section projects-section" id="proyek">

        <div class="section-title">

            <p>♡ My little works</p>

            <h2>Proyek Saya</h2>

            <span>
                Klik tombol demo untuk mencoba proyeknya ✨
            </span>

        </div>


        <div class="project-grid">

            <!-- KALKULATOR -->

            <article class="project-card">

                <div class="project-icon purple-icon">
                    🧮
                </div>

                <div class="project-content">

                    <span class="project-number">01</span>

                    <h3>Kalkulator Mini</h3>

                    <p>
                        Kalkulator sederhana yang dapat
                        melakukan operasi hitung dasar.
                    </p>

                    <div class="project-tags">
                        <span>HTML</span>
                        <span>CSS</span>
                        <span>JavaScript</span>
                    </div>

                    <button
                        class="demo-button"
                        onclick="openCalculator()"
                    >
                        Coba Kalkulator →
                    </button>

                </div>

            </article>


            <!-- JADWAL -->

            <article class="project-card">

                <div class="project-icon pink-icon">
                    📚
                </div>

                <div class="project-content">

                    <span class="project-number">02</span>

                    <h3>Jadwal Belajar</h3>

                    <p>
                        Tambahkan jadwal belajar dan
                        hapus jadwal yang sudah selesai.
                    </p>

                    <div class="project-tags">
                        <span>HTML</span>
                        <span>CSS</span>
                        <span>JavaScript</span>
                    </div>

                    <button
                        class="demo-button"
                        onclick="openSchedule()"
                    >
                        Coba Jadwal →
                    </button>

                </div>

            </article>


            <!-- TODO -->

            <article class="project-card">

                <div class="project-icon blue-icon">
                    🎀
                </div>

                <div class="project-content">

                    <span class="project-number">03</span>

                    <h3>To Do List</h3>

                    <p>
                        Tambahkan tugas, centang tugas
                        yang selesai, dan hapus tugas.
                    </p>

                    <div class="project-tags">
                        <span>JavaScript</span>
                        <span>UI/UX</span>
                        <span>Responsive</span>
                    </div>

                    <button
                        class="demo-button"
                        onclick="openTodo()"
                    >
                        Coba To Do List →
                    </button>

                </div>

            </article>

        </div>

    </section>


    <!-- SKILLS -->

    <section class="section">

        <div class="section-title">

            <p>♡ What I learn</p>

            <h2>My Skills</h2>

        </div>


        <div class="skills-container">

            <div>
                <div class="skill-info">
                    <span>HTML</span>
                    <span>80%</span>
                </div>

                <div class="skill-bar">
                    <div class="skill-progress html-progress"></div>
                </div>
            </div>


            <div>
                <div class="skill-info">
                    <span>CSS</span>
                    <span>75%</span>
                </div>

                <div class="skill-bar">
                    <div class="skill-progress css-progress"></div>
                </div>
            </div>


            <div>
                <div class="skill-info">
                    <span>JavaScript</span>
                    <span>60%</span>
                </div>

                <div class="skill-bar">
                    <div class="skill-progress js-progress"></div>
                </div>
            </div>


            <div>
                <div class="skill-info">
                    <span>UI/UX Design</span>
                    <span>70%</span>
                </div>

                <div class="skill-bar">
                    <div class="skill-progress ui-progress"></div>
                </div>
            </div>

        </div>

    </section>


    <!-- KONTAK -->

    <section class="section" id="kontak">

        <div class="contact-card">

            <div class="section-title">

                <p>♡ Let's connect</p>

                <h2>Hubungi Saya</h2>

            </div>

            <p>
                Jangan ragu untuk menghubungiku
                melalui media sosial atau email 💜
            </p>

            <div class="contact-list">

                <a
                    href="mailto:safaafaa544@gmail.com"
                    class="contact-item"
                >
                    <span>📧</span>

                    <span>
                        <small>Email</small>
                        safaafaa544@gmail.com
                    </span>
                </a>


                <a
                    href="https://instagram.com/owwzzz_"
                    target="_blank"
                    rel="noopener noreferrer"
                    class="contact-item"
                >
                    <span>📷</span>

                    <span>
                        <small>Instagram</small>
                        @owwzzz_
                    </span>
                </a>

            </div>

        </div>

    </section>

</main>


<footer class="footer">

    <p>
        Made with ♡ by Lola Nadira Syafah
    </p>

    <p>
        © 2026 • X RPL 3 • Absen 39
    </p>

</footer>


<!-- SCROLL TOP -->

<button
    class="scroll-top"
    id="scroll-top"
>
    ↑
</button>


<!-- MODAL KALKULATOR -->

<div class="modal" id="calculator-modal">

    <div class="modal-box">

        <h3>🧮 Kalkulator Mini</h3>

        <div class="calculator">

            <input
                type="text"
                class="calculator-display"
                id="calculator-display"
                value="0"
                readonly
            >

            <div class="calculator-buttons">

                <button onclick="clearCalculator()">C</button>
                <button onclick="deleteNumber()">⌫</button>
                <button class="operator" onclick="addOperator('%')">%</button>
                <button class="operator" onclick="addOperator('/')">÷</button>

                <button onclick="addNumber('7')">7</button>
                <button onclick="addNumber('8')">8</button>
                <button onclick="addNumber('9')">9</button>
                <button class="operator" onclick="addOperator('*')">×</button>

                <button onclick="addNumber('4')">4</button>
                <button onclick="addNumber('5')">5</button>
                <button onclick="addNumber('6')">6</button>
                <button class="operator" onclick="addOperator('-')">−</button>

                <button onclick="addNumber('1')">1</button>
                <button onclick="addNumber('2')">2</button>
                <button onclick="addNumber('3')">3</button>
                <button class="operator" onclick="addOperator('+')">+</button>

                <button onclick="addNumber('0')">0</button>
                <button onclick="addNumber('.')">.</button>
                <button
                    class="equal"
                    onclick="calculate()"
                    style="grid-column: span 2;"
                >
                    =
                </button>

            </div>

        </div>

        <button
            class="close-modal"
            onclick="closeAllModal()"
        >
            Tutup
        </button>

    </div>

</div>


<!-- MODAL JADWAL -->

<div class="modal" id="schedule-modal">

    <div class="modal-box">

        <h3>📚 Jadwal Belajar</h3>

        <div class="form-group">

            <input
                type="text"
                id="schedule-input"
                placeholder="Contoh: Belajar JavaScript"
            >

            <button
                class="add-button"
                onclick="addSchedule()"
            >
                Tambah
            </button>

        </div>

        <div
            class="schedule-list"
            id="schedule-list"
        ></div>

        <button
            class="close-modal"
            onclick="closeAllModal()"
        >
            Tutup
        </button>

    </div>

</div>


<!-- MODAL TODO -->

<div class="modal" id="todo-modal">

    <div class="modal-box">

        <h3>🎀 To Do List</h3>

        <div class="todo-input">

            <input
                type="text"
                id="todo-input"
                placeholder="Tulis tugas kamu..."
            >

            <button
                class="add-button"
                onclick="addTodo()"
            >
                Tambah
            </button>

        </div>

        <div
            class="todo-list"
            id="todo-list"
        ></div>

        <button
            class="close-modal"
            onclick="closeAllModal()"
        >
            Tutup
        </button>

    </div>

</div>


<script>

    /* =========================
       HAMBURGER MENU
    ========================= */

    const menuToggle =
        document.getElementById("menu-toggle");

    const navMenu =
        document.getElementById("nav-menu");

    menuToggle.addEventListener("click", function () {

        navMenu.classList.toggle("active");

        menuToggle.textContent =
            navMenu.classList.contains("active")
                ? "✕"
                : "☰";

    });


    document.querySelectorAll(".nav-menu a")
        .forEach(function(link) {

            link.addEventListener("click", function() {

                navMenu.classList.remove("active");

                menuToggle.textContent = "☰";

            });

        });


    /* =========================
       DARK MODE
    ========================= */

    const themeToggle =
        document.getElementById("theme-toggle");

    themeToggle.addEventListener("click", function() {

        document.body.classList.toggle("dark-mode");

        themeToggle.textContent =
            document.body.classList.contains("dark-mode")
                ? "☀️"
                : "🌙";

    });


    /* =========================
       SCROLL TOP
    ========================= */

    const scrollTop =
        document.getElementById("scroll-top");

    window.addEventListener("scroll", function() {

        if (window.scrollY > 400) {

            scrollTop.classList.add("show");

        } else {

            scrollTop.classList.remove("show");

        }

    });


    scrollTop.addEventListener("click", function() {

        window.scrollTo({
            top: 0,
            behavior: "smooth"
        });

    });


    /* =========================
       MODAL
    ========================= */

    function closeAllModal() {

        document.querySelectorAll(".modal")
            .forEach(function(modal) {

                modal.classList.remove("active");

            });

    }


    function openCalculator() {

        closeAllModal();

        document
            .getElementById("calculator-modal")
            .classList.add("active");

    }


    function openSchedule() {

        closeAllModal();

        document
            .getElementById("schedule-modal")
            .classList.add("active");

    }


    function openTodo() {

        closeAllModal();

        document
            .getElementById("todo-modal")
            .classList.add("active");

    }


    document.querySelectorAll(".modal")
        .forEach(function(modal) {

            modal.addEventListener("click", function(event) {

                if (event.target === modal) {

                    closeAllModal();

                }

            });

        });


    /* =========================
       KALKULATOR
    ========================= */

    const display =
        document.getElementById("calculator-display");

    let calculatorValue = "";


    function addNumber(number) {

        calculatorValue += number;

        display.value = calculatorValue || "0";

    }


    function addOperator(operator) {

        if (calculatorValue === "") {
            return;
        }

        const lastCharacter =
            calculatorValue.slice(-1);

        if ("+-*/%".includes(lastCharacter)) {

            calculatorValue =
                calculatorValue.slice(0, -1);

        }

        calculatorValue += operator;

        display.value = calculatorValue;

    }


    function clearCalculator() {

        calculatorValue = "";

        display.value = "0";

    }


    function deleteNumber() {

        calculatorValue =
            calculatorValue.slice(0, -1);

        display.value =
            calculatorValue || "0";

    }


    function calculate() {

        if (calculatorValue === "") {
            return;
        }

        try {

            /*
                Function digunakan hanya untuk
                menghitung ekspresi kalkulator
                yang dibentuk dari tombol di atas.
            */

            const result =
                Function(
                    "return " + calculatorValue
                )();

            if (!Number.isFinite(result)) {

                display.value = "Error";

                calculatorValue = "";

                return;

            }

            calculatorValue =
                String(result);

            display.value =
                calculatorValue;

        } catch (error) {

            display.value = "Error";

            calculatorValue = "";

        }

    }


    /* =========================
       JADWAL BELAJAR
    ========================= */

    const scheduleInput =
        document.getElementById("schedule-input");

    const scheduleList =
        document.getElementById("schedule-list");


    function addSchedule() {

        const text =
            scheduleInput.value.trim();

        if (text === "") {

            alert("Tulis jadwal terlebih dahulu!");

            return;

        }

        const item =
            document.createElement("div");

        item.className =
            "schedule-item";

        item.innerHTML = `
            <span>📚 ${text}</span>
            <button
                class="delete-small"
                onclick="this.parentElement.remove()"
            >
                Hapus
            </button>
        `;

        scheduleList.appendChild(item);

        scheduleInput.value = "";

        scheduleInput.focus();

    }


    scheduleInput.addEventListener("keydown", function(event) {

        if (event.key === "Enter") {

            addSchedule();

        }

    });


    /* =========================
       TO DO LIST
    ========================= */

    const todoInput =
        document.getElementById("todo-input");

    const todoList =
        document.getElementById("todo-list");


    function addTodo() {

        const text =
            todoInput.value.trim();

        if (text === "") {

            alert("Tulis tugas terlebih dahulu!");

            return;

        }

        const item =
            document.createElement("div");

        item.className =
            "todo-item";

        item.innerHTML = `
            <input
                type="checkbox"
                class="todo-check"
                onchange="completeTodo(this)"
            >

            <span>${text}</span>

            <button
                class="delete-small"
                onclick="this.parentElement.remove()"
            >
                Hapus
            </button>
        `;

        todoList.appendChild(item);

        todoInput.value = "";

        todoInput.focus();

    }


    function completeTodo(checkbox) {

        const item =
            checkbox.parentElement;

        if (checkbox.checked) {

            item.classList.add("completed");

        } else {

            item.classList.remove("completed");

        }

    }


    todoInput.addEventListener("keydown", function(event) {

        if (event.key === "Enter") {

            addTodo();

        }

    });

</script>

</body>
</html>

