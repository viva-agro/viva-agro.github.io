<!DOCTYPE html>
<html lang="az">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Viva Agro | Müasir Kənd Təsərrüfatı</title>

    <meta name="description"
          content="Viva Agro — müasir, dayanıqlı və innovativ kənd təsərrüfatı.">

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: Arial, Helvetica, sans-serif;
            color: #263326;
            line-height: 1.6;
            background: #ffffff;
        }

        a {
            text-decoration: none;
            color: inherit;
        }

        /* =========================
           NAVBAR
        ========================= */

        nav {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            background: rgba(255,255,255,0.97);
            border-bottom: 1px solid #e5e5e5;
        }

        .nav-container {
            max-width: 1200px;
            height: 75px;
            margin: auto;
            padding: 0 25px;

            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .logo {
            font-size: 28px;
            font-weight: 800;
            color: #236b36;
            letter-spacing: -1px;
        }

        .logo span {
            color: #8aaa3c;
        }

        .nav-links {
            display: flex;
            align-items: center;
            gap: 28px;
            list-style: none;
        }

        .nav-links a {
            font-size: 15px;
            font-weight: 600;
            color: #344434;
            transition: 0.3s;
        }

        .nav-links a:hover {
            color: #3f873f;
        }

        .nav-button {
            background: #236b36;
            color: white !important;
            padding: 11px 21px;
            border-radius: 25px;
        }

        .nav-button:hover {
            background: #174c25;
        }

        /* =========================
           HERO
        ========================= */

        .hero {
            min-height: 100vh;
            padding-top: 75px;

            background:
                linear-gradient(
                    rgba(20,55,25,0.58),
                    rgba(20,55,25,0.58)
                ),
                url("https://images.unsplash.com/photo-1500382017468-9049fed747ef?auto=format&fit=crop&w=2000&q=85");

            background-size: cover;
            background-position: center;

            display: flex;
            align-items: center;
        }

        .hero-content {
            max-width: 1200px;
            width: 100%;
            margin: auto;
            padding: 80px 25px;
            color: white;
        }

        .hero-small {
            text-transform: uppercase;
            letter-spacing: 3px;
            font-size: 14px;
            font-weight: 700;
            margin-bottom: 20px;
        }

        .hero h1 {
            max-width: 850px;
            font-size: clamp(45px, 7vw, 82px);
            line-height: 1.05;
            margin-bottom: 25px;
        }

        .hero h1 span {
            color: #b7d66a;
        }

        .hero p {
            max-width: 650px;
            font-size: 19px;
            margin-bottom: 35px;
        }

        .hero-buttons {
            display: flex;
            gap: 15px;
            flex-wrap: wrap;
        }

        .button {
            display: inline-block;
            padding: 15px 28px;
            border-radius: 30px;
            font-weight: 700;
            transition: 0.3s;
        }

        .button-primary {
            background: #b7d66a;
            color: #1c4825;
        }

        .button-primary:hover {
            background: white;
            transform: translateY(-2px);
        }

        .button-secondary {
            border: 2px solid white;
            color: white;
        }

        .button-secondary:hover {
            background: white;
            color: #236b36;
        }

        /* =========================
           GENERAL
        ========================= */

        section {
            padding: 100px 25px;
        }

        .container {
            max-width: 1200px;
            margin: auto;
        }

        .section-label {
            color: #6d9636;
            font-size: 14px;
            font-weight: 800;
            text-transform: uppercase;
            letter-spacing: 2px;
            margin-bottom: 12px;
        }

        .section-title {
            font-size: 45px;
            line-height: 1.15;
            color: #203722;
            margin-bottom: 20px;
        }

        .section-text {
            max-width: 700px;
            color: #687168;
            font-size: 17px;
        }

        /* =========================
           HAQQIMIZDA
        ========================= */

        .about {
            background: #f7f9f4;
        }

        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 70px;
            align-items: center;
        }

        .about-image {
            width: 100%;
            min-height: 500px;
            border-radius: 20px;

            background:
                url("https://images.unsplash.com/photo-1464226184884-fa280b87c399?auto=format&fit=crop&w=1200&q=85");

            background-size: cover;
            background-position: center;
        }

        .about-content p {
            color: #657065;
            margin-bottom: 20px;
            font-size: 17px;
        }

        .stats {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
            margin-top: 35px;
        }

        .stat {
            background: white;
            padding: 22px;
            border-radius: 12px;
            border: 1px solid #e4e8df;
        }

        .stat strong {
            display: block;
            font-size: 30px;
            color: #236b36;
        }

        .stat span {
            font-size: 13px;
            color: #727a72;
        }

        /* =========================
           FƏALİYYƏT
        ========================= */

        .activities {
            background: white;
        }

        .activities-header {
            text-align: center;
            margin-bottom: 50px;
        }

        .activities-header .section-text {
            margin: auto;
        }

        .cards {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 25px;
        }

        .card {
            padding: 35px;
            border-radius: 18px;
            background: #f7f9f4;
            border: 1px solid #e6e9e1;
            transition: 0.3s;
        }

        .card:hover {
            transform: translateY(-8px);
            box-shadow: 0 15px 35px rgba(0,0,0,0.08);
        }

        .card-icon {
            font-size: 42px;
            margin-bottom: 20px;
        }

        .card h3 {
            font-size: 23px;
            color: #29442d;
            margin-bottom: 12px;
        }

        .card p {
            color: #6c746c;
        }

        /* =========================
           MƏHSULLAR
        ========================= */

        .products {
            background: #edf3e7;
        }

        .product-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 25px;
            margin-top: 50px;
        }

        .product {
            background: white;
            border-radius: 18px;
            overflow: hidden;
            box-shadow: 0 8px 25px rgba(0,0,0,0.05);
        }

        .product-image {
            height: 260px;
            background-size: cover;
            background-position: center;
        }

        .product:nth-child(1) .product-image {
            background-image:
                url("https://images.unsplash.com/photo-1608797178974-15b35a64ede9?auto=format&fit=crop&w=1000&q=85");
        }

        .product:nth-child(2) .product-image {
            background-image:
                url("https://images.unsplash.com/photo-1501004318641-b39e6451bec6?auto=format&fit=crop&w=1000&q=85");
        }

        .product:nth-child(3) .product-image {
            background-image:
                url("https://images.unsplash.com/photo-1553279768-865429fa0078?auto=format&fit=crop&w=1000&q=85");
        }

        .product-content {
            padding: 25px;
        }

        .product-content h3 {
            color: #29442d;
            font-size: 22px;
            margin-bottom: 8px;
        }

        .product-content p {
            color: #707870;
        }

        /* =========================
           DAYANIQLILIQ
        ========================= */

        .sustainability {
            background: #214c2a;
            color: white;
        }

        .sustainability .section-title {
            color: white;
        }

        .sustainability .section-text {
            color: #d6e0d5;
        }

        .sustainability-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 70px;
            align-items: center;
        }

        .sustainability-image {
            min-height: 480px;
            border-radius: 20px;

            background:
                url("https://images.unsplash.com/photo-1523742819016-8f39d1d7d5e0?auto=format&fit=crop&w=1200&q=85");

            background-size: cover;
            background-position: center;
        }

        .sustainability-list {
            margin-top: 30px;
            list-style: none;
        }

        .sustainability-list li {
            padding: 15px 0;
            border-bottom: 1px solid rgba(255,255,255,0.15);
            font-size: 17px;
        }

        .sustainability-list li::before {
            content: "✓";
            color: #b7d66a;
            font-weight: bold;
            margin-right: 12px;
        }

        /* =========================
           ƏLAQƏ
        ========================= */

        .contact {
            background: #f7f9f4;
        }

        .contact-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 70px;
        }

        .contact-info {
            margin-top: 35px;
        }

        .contact-item {
            margin-bottom: 25px;
        }

        .contact-item strong {
            display: block;
            color: #29442d;
            margin-bottom: 4px;
        }

        .contact-item span {
            color: #6d756d;
        }

        form {
            background: white;
            padding: 35px;
            border-radius: 18px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.05);
        }

        input,
        textarea {
            width: 100%;
            padding: 15px;
            margin-bottom: 15px;
            border: 1px solid #dfe4dc;
            border-radius: 8px;
            font-family: inherit;
            font-size: 15px;
        }

        textarea {
            min-height: 150px;
            resize: vertical;
        }

        input:focus,
        textarea:focus {
            outline: 2px solid #b7d66a;
            border-color: transparent;
        }

        .submit-button {
            border: none;
            cursor: pointer;
            width: 100%;
        }

        /* =========================
           FOOTER
        ========================= */

        footer {
            background: #17291a;
            color: white;
            padding: 50px 25px 25px;
        }

        .footer-grid {
            max-width: 1200px;
            margin: auto;

            display: grid;
            grid-template-columns: 2fr 1fr 1fr;
            gap: 50px;

            padding-bottom: 40px;
        }

        footer .logo {
            color: white;
            margin-bottom: 15px;
        }

        footer p {
            color: #aeb9ad;
            max-width: 450px;
        }

        footer h4 {
            margin-bottom: 15px;
        }

        footer ul {
            list-style: none;
        }

        footer li {
            margin-bottom: 8px;
            color: #aeb9ad;
        }

        .copyright {
            max-width: 1200px;
            margin: auto;
            padding-top: 25px;
            border-top: 1px solid rgba(255,255,255,0.1);
            color: #879487;
            font-size: 13px;
        }

        /* =========================
           MOBILE
        ========================= */

        @media (max-width: 850px) {

            .nav-links {
                display: none;
            }

            .hero h1 {
                font-size: 48px;
            }

            .about-grid,
            .sustainability-grid,
            .contact-grid {
                grid-template-columns: 1fr;
            }

            .cards,
            .product-grid {
                grid-template-columns: 1fr;
            }

            .stats {
                grid-template-columns: 1fr;
            }

            .footer-grid {
                grid-template-columns: 1fr;
            }

            section {
                padding: 70px 20px;
            }

            .section-title {
                font-size: 36px;
            }
        }
    </style>
</head>


<body>

<!-- =========================
     NAVİQASİYA
========================= -->

<nav>

    <div class="nav-container">

        <div class="logo">
            VIVA<span>AGRO</span>
        </div>

        <ul class="nav-links">

            <li>
                <a href="#home">Ana səhifə</a>
            </li>

            <li>
                <a href="#about">Haqqımızda</a>
            </li>

            <li>
                <a href="#activities">Fəaliyyətimiz</a>
            </li>

            <li>
                <a href="#products">Məhsullar</a>
            </li>

            <li>
                <a href="#sustainability">Dayanıqlılıq</a>
            </li>

            <li>
                <a class="nav-button" href="#contact">
                    Əlaqə
                </a>
            </li>

        </ul>

    </div>

</nav>


<!-- =========================
     ANA SƏHİFƏ
========================= -->

<section class="hero" id="home">

    <div class="hero-content">

        <div class="hero-small">
            Kənd təsərrüfatı • İnnovasiya • Dayanıqlılıq
        </div>

        <h1>
            Kənd təsərrüfatının
            <span>gələcəyini</span>
            birlikdə yetişdiririk.
        </h1>

        <p>
            Viva Agro müasir kənd təsərrüfatı texnologiyalarını,
            səmərəli resurs idarəçiliyini və dayanıqlı istehsal
            prinsiplərini birləşdirərək kənd təsərrüfatında
            uzunmüddətli dəyər yaradır.
        </p>

        <div class="hero-buttons">

            <a href="#about"
               class="button button-primary">
                Viva Agro haqqında
            </a>

            <a href="#contact"
               class="button button-secondary">
                Bizimlə əlaqə
            </a>

        </div>

    </div>

</section>


<!-- =========================
     HAQQIMIZDA
========================= -->

<section class="about" id="about">

    <div class="container about-grid">

        <div class="about-image"></div>

        <div class="about-content">

            <div class="section-label">
                Haqqımızda
            </div>

            <h2 class="section-title">
                Kənd təsərrüfatına uzunmüddətli baxış.
            </h2>

            <p>
                Viva Agro müasir və səmərəli kənd təsərrüfatı
                fəaliyyətinin inkişafına yönəlmiş aqrar şirkətdir.
            </p>

            <p>
                Fəaliyyətimizdə müasir əkinçilik metodlarından,
                innovativ texnologiyalardan və səmərəli resurs
                idarəetməsindən istifadə etməyə çalışırıq.
            </p>

            <p>
                Biz kənd təsərrüfatına yalnız məhsul istehsalı
                kimi deyil, torpağın, insanların və gələcək
                nəsillərin rifahına xidmət edən uzunmüddətli
                biznes sahəsi kimi baxırıq.
            </p>

            <div class="stats">

                <div class="stat">
                    <strong>100+</strong>
                    <span>
                        Hektar kənd təsərrüfatı potensialı
                    </span>
                </div>

                <div class="stat">
                    <strong>24/7</strong>
                    <span>
                        Fəaliyyətə davamlı yanaşma
                    </span>
                </div>

                <div class="stat">
                    <strong>100%</strong>
                    <span>
                        Dayanıqlı inkişaf yönümlü
                    </span>
                </div>

            </div>

        </div>

    </div>

</section>


<!-- =========================
     FƏALİYYƏTİMİZ
========================= -->

<section class="activities" id="activities">

    <div class="container">

        <div class="activities-header">

            <div class="section-label">
                Fəaliyyətimiz
            </div>

            <h2 class="section-title">
                Aqrar fəaliyyət istiqamətlərimiz
            </h2>

            <p class="section-text">
                Torpağın hazırlanmasından məhsul istehsalına,
                suvarmadan logistika və bazarlara çıxışa qədər
                kənd təsərrüfatı fəaliyyətinin müxtəlif
                istiqamətlərində inkişaf edirik.
            </p>

        </div>


        <div class="cards">

            <div class="card">

                <div class="card-icon">🌱</div>

                <h3>Bitkiçilik</h3>

                <p>
                    Müasir aqrotexniki üsullardan istifadə etməklə
                    yüksək məhsuldarlığa və keyfiyyətə yönəlmiş
                    bitkiçilik fəaliyyəti.
                </p>

            </div>


            <div class="card">

                <div class="card-icon">🌳</div>

                <h3>Bağçılıq</h3>

                <p>
                    Uzunmüddətli məhsuldarlıq və keyfiyyət
                    məqsədi ilə meyvə bağlarının yaradılması
                    və idarə olunması.
                </p>

            </div>


            <div class="card">

                <div class="card-icon">💧</div>

                <h3>Suvarma sistemləri</h3>

                <p>
                    Su ehtiyatlarından səmərəli istifadə üçün
                    müasir suvarma və su idarəetmə sistemlərinin
                    tətbiqi.
                </p>

            </div>


            <div class="card">

                <div class="card-icon">🚜</div>

                <h3>Müasir aqrotexnologiyalar</h3>

                <p>
                    Müasir kənd təsərrüfatı texnikası, texnologiya
                    və məlumat əsaslı qərarvermə ilə
                    istehsal səmərəliliyinin artırılması.
                </p>

            </div>


            <div class="card">

                <div class="card-icon">📦</div>

                <h3>Aqrar təchizat zənciri</h3>

                <p>
                    Kənd təsərrüfatı məhsullarının istehsal,
                    saxlama, daşınma və satış mərhələlərinin
                    əlaqələndirilməsi.
                </p>

            </div>


            <div class="card">

                <div class="card-icon">🌍</div>

                <h3>Yerli və ixrac bazarları</h3>

                <p>
                    Azərbaycan kənd təsərrüfatı məhsullarının
                    yerli və regional bazarlara çıxarılması
                    üçün imkanların inkişaf etdirilməsi.
                </p>

            </div>

        </div>

    </div>

</section>


<!-- =========================
     MƏHSULLAR
========================= -->

<section class="products" id="products">

    <div class="container">

        <div class="section-label">
            Məhsullarımız
        </div>

        <h2 class="section-title">
            Torpaqdan bazara qədər.
        </h2>

        <p class="section-text">
            Aqrar fəaliyyətimizin əsas istiqamətlərinə
            müxtəlif kənd təsərrüfatı məhsullarının istehsalı
            və bazarlara çıxarılması daxildir.
        </p>


        <div class="product-grid">

            <div class="product">

                <div class="product-image"></div>

                <div class="product-content">

                    <h3>Fındıq</h3>

                    <p>
                        Yüksək keyfiyyətli fındıq istehsalına
                        yönəlmiş bağçılıq fəaliyyəti.
                    </p>

                </div>

            </div>


            <div class="product">

                <div class="product-image"></div>

                <div class="product-content">

                    <h3>Yonca və yem bitkiləri</h3>

                    <p>
                        Heyvandarlıq və aqrar təchizat zənciri
                        üçün yem bitkilərinin istehsalı.
                    </p>

                </div>

            </div>


            <div class="product">

                <div class="product-image"></div>

                <div class="product-content">

                    <h3>Kənd təsərrüfatı məhsulları</h3>

                    <p>
                        Yerli və regional bazarlar üçün
                        müxtəlif kənd təsərrüfatı məhsullarının
                        istehsalı.
                    </p>

                </div>

            </div>

        </div>

    </div>

</section>


<!-- =========================
     DAYANIQLI İNKİŞAF
========================= -->

<section class="sustainability"
         id="sustainability">

    <div class="container sustainability-grid">

        <div class="sustainability-image"></div>

        <div>

            <div class="section-label">
                Dayanıqlı inkişaf
            </div>

            <h2 class="section-title">
                Bu gün əkirik, gələcəyi yetişdiririk.
            </h2>

            <p class="section-text">
                Məqsədimiz məhsuldarlıq, iqtisadi səmərəlilik
                və ətraf mühitə məsuliyyət arasında balans
                yaradan kənd təsərrüfatı sistemləri formalaşdırmaqdır.
            </p>

            <ul class="sustainability-list">

                <li>
                    Su ehtiyatlarından səmərəli istifadə
                </li>

                <li>
                    Torpaqların məsuliyyətli idarə olunması
                </li>

                <li>
                    Müasir suvarma texnologiyaları
                </li>

                <li>
                    Kənd təsərrüfatında məhsuldarlığın artırılması
                </li>

                <li>
                    Torpağın uzunmüddətli sağlamlığının qorunması
                </li>

                <li>
                    Texnologiya və məlumat əsaslı qərarvermə
                </li>

            </ul>

        </div>

    </div>

</section>


<!-- =========================
     ƏLAQƏ
========================= -->

<section class="contact" id="contact">

    <div class="container contact-grid">

        <div>

            <div class="section-label">
                Əlaqə
            </div>

            <h2 class="section-title">
                Birlikdə inkişaf edək.
            </h2>

            <p class="section-text">
                Aqrar layihələr, investisiya imkanları,
                məhsullarımız və əməkdaşlıq təklifləri
                barədə bizimlə əlaqə saxlaya bilərsiniz.
            </p>

            <div class="contact-info">

                <div class="contact-item">
                    <strong>Şirkət</strong>
                    <span>Viva Agro</span>
                </div>

                <div class="contact-item">
                    <strong>E-poçt</strong>
                    <span>info@viva-agro.com</span>
                </div>

                <div class="contact-item">
                    <strong>Ölkə</strong>
                    <span>Azərbaycan</span>
                </div>

                <div class="contact-item">
                    <strong>Fəaliyyət sahəsi</strong>
                    <span>
                        Kənd təsərrüfatı • Aqrobiznes • Aqrar məhsullar
                    </span>
                </div>

            </div>

        </div>


        <form action="mailto:info@viva-agro.com"
              method="post"
              enctype="text/plain">

            <input
                type="text"
                name="Ad"
                placeholder="Adınız"
                required
            >

            <input
                type="email"
                name="Email"
                placeholder="E-poçt ünvanınız"
                required
            >

            <input
                type="text"
                name="Sirket"
                placeholder="Şirkətiniz"
            >

            <textarea
                name="Mesaj"
                placeholder="Mesajınız"
                required
            ></textarea>

            <button
                type="submit"
                class="button button-primary submit-button">
                Mesaj göndər
            </button>

        </form>

    </div>

</section>


<!-- =========================
     FOOTER
========================= -->

<footer>

    <div class="footer-grid">

        <div>

            <div class="logo">
                VIVA<span>AGRO</span>
            </div>

            <p>
                Dayanıqlı kənd təsərrüfatı,
                innovasiya və gələcəyə yönəlmiş inkişaf.
            </p>

        </div>


        <div>

            <h4>Naviqasiya</h4>

            <ul>

                <li>
                    <a href="#home">Ana səhifə</a>
                </li>

                <li>
                    <a href="#about">Haqqımızda</a>
                </li>

                <li>
                    <a href="#activities">Fəaliyyətimiz</a>
                </li>

                <li>
                    <a href="#products">Məhsullar</a>
                </li>

                <li>
                    <a href="#contact">Əlaqə</a>
                </li>

            </ul>

        </div>


        <div>

            <h4>Viva Agro</h4>

            <ul>

                <li>Kənd təsərrüfatı</li>

                <li>Bitkiçilik</li>

                <li>Bağçılıq</li>

                <li>Aqrobiznes</li>

                <li>Dayanıqlı inkişaf</li>

            </ul>

        </div>

    </div>


    <div class="copyright">
        © 2026 Viva Agro. Bütün hüquqlar qorunur.
    </div>

</footer>

</body>
</html>
