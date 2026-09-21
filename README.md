<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>WAŁBRZYCH — Polish × English Student Exchange</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Manrope:wght@500;600;700;800&display=swap" rel="stylesheet">

<style>

:root{
    --bg:#070b18;
    --bg2:#0c1225;
    --card:rgba(255,255,255,.065);
    --card2:rgba(255,255,255,.09);
    --white:#ffffff;
    --text:#e9edff;
    --muted:#98a2bd;
    --blue:#5b8cff;
    --cyan:#42d9ff;
    --purple:#9b6cff;
    --pink:#e86cff;
    --green:#55e6b0;
    --yellow:#ffd166;
    --border:rgba(255,255,255,.12);
    --shadow:0 25px 80px rgba(0,0,0,.35);
}

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

html{
    scroll-behavior:smooth;
}

body{
    font-family:"DM Sans",sans-serif;
    background:
        radial-gradient(circle at 10% 10%, rgba(91,140,255,.16), transparent 30%),
        radial-gradient(circle at 90% 20%, rgba(155,108,255,.15), transparent 28%),
        radial-gradient(circle at 50% 90%, rgba(66,217,255,.08), transparent 30%),
        var(--bg);
    color:var(--text);
    overflow-x:hidden;
}

body::before{
    content:"";
    position:fixed;
    inset:0;
    pointer-events:none;
    background-image:
        linear-gradient(rgba(255,255,255,.025) 1px,transparent 1px),
        linear-gradient(90deg,rgba(255,255,255,.025) 1px,transparent 1px);
    background-size:50px 50px;
    mask-image:linear-gradient(to bottom,black,transparent 90%);
}

/* NAVIGATION */

nav{
    position:fixed;
    top:18px;
    left:50%;
    transform:translateX(-50%);
    width:min(1180px,calc(100% - 30px));
    z-index:1000;
    background:rgba(9,14,31,.78);
    backdrop-filter:blur(20px);
    border:1px solid var(--border);
    border-radius:22px;
    padding:12px 16px;
    display:flex;
    align-items:center;
    justify-content:space-between;
    transition:.3s;
}

.logo{
    font-family:"Manrope";
    font-weight:800;
    font-size:19px;
    letter-spacing:-.5px;
}

.logo span{
    background:linear-gradient(90deg,var(--blue),var(--cyan),var(--purple));
    -webkit-background-clip:text;
    color:transparent;
}

.navlinks{
    display:flex;
    gap:5px;
}

.navlinks a{
    color:#aeb7d0;
    text-decoration:none;
    padding:10px 13px;
    border-radius:12px;
    font-size:13px;
    font-weight:600;
    transition:.25s;
}

.navlinks a:hover{
    color:white;
    background:rgba(255,255,255,.08);
}

.nav-button{
    border:0;
    color:white;
    background:linear-gradient(135deg,var(--blue),var(--purple));
    padding:11px 17px;
    border-radius:13px;
    font-weight:700;
    cursor:pointer;
    box-shadow:0 8px 25px rgba(91,140,255,.25);
}

/* HERO */

.hero{
    min-height:100vh;
    max-width:1180px;
    margin:auto;
    padding:160px 25px 100px;
    display:grid;
    grid-template-columns:1.2fr .8fr;
    align-items:center;
    gap:60px;
}

.badge{
    display:inline-flex;
    align-items:center;
    gap:9px;
    padding:8px 13px;
    border:1px solid var(--border);
    border-radius:999px;
    background:rgba(255,255,255,.045);
    color:#c5cce0;
    font-size:12px;
    font-weight:700;
    letter-spacing:.5px;
    margin-bottom:25px;
}

.badge-dot{
    width:8px;
    height:8px;
    border-radius:50%;
    background:var(--green);
    box-shadow:0 0 15px var(--green);
}

.hero h1{
    font-family:"Manrope";
    font-size:clamp(50px,7vw,92px);
    line-height:.95;
    letter-spacing:-5px;
    max-width:800px;
}

.gradient{
    background:linear-gradient(
        90deg,
        #fff 0%,
        #72a1ff 35%,
        #66e4ff 65%,
        #b17aff 100%
    );
    -webkit-background-clip:text;
    color:transparent;
}

.hero p{
    margin-top:28px;
    max-width:650px;
    color:var(--muted);
    line-height:1.8;
    font-size:17px;
}

.hero-buttons{
    display:flex;
    gap:12px;
    margin-top:34px;
    flex-wrap:wrap;
}

.primary,
.secondary{
    padding:15px 22px;
    border-radius:15px;
    font-weight:700;
    cursor:pointer;
    text-decoration:none;
    transition:.25s;
}

.primary{
    background:linear-gradient(135deg,var(--blue),var(--purple));
    color:white;
    border:0;
    box-shadow:0 15px 40px rgba(91,140,255,.2);
}

.secondary{
    border:1px solid var(--border);
    color:white;
    background:rgba(255,255,255,.04);
}

.primary:hover,
.secondary:hover{
    transform:translateY(-3px);
}

/* HERO CARD */

.hero-card{
    position:relative;
    min-height:470px;
    border-radius:35px;
    border:1px solid var(--border);
    background:
        linear-gradient(145deg,rgba(91,140,255,.13),rgba(155,108,255,.08)),
        rgba(255,255,255,.035);
    box-shadow:var(--shadow);
    overflow:hidden;
    padding:30px;
}

.hero-card::before{
    content:"";
    position:absolute;
    width:260px;
    height:260px;
    border-radius:50%;
    background:var(--purple);
    filter:blur(100px);
    opacity:.25;
    top:-80px;
    right:-80px;
}

.hero-card-top{
    position:relative;
    z-index:2;
    display:flex;
    justify-content:space-between;
}

.small-label{
    color:#8e99b5;
    font-size:10px;
    font-weight:800;
    letter-spacing:2px;
}

.year{
    font-size:13px;
    font-weight:800;
    color:var(--cyan);
}

.globe{
    position:absolute;
    width:260px;
    height:260px;
    border:1px solid rgba(255,255,255,.13);
    border-radius:50%;
    left:50%;
    top:50%;
    transform:translate(-50%,-50%);
}

.globe::before,
.globe::after{
    content:"";
    position:absolute;
    inset:35px;
    border:1px solid rgba(255,255,255,.1);
    border-radius:50%;
}

.globe::after{
    inset:70px;
}

.hero-card-content{
    position:absolute;
    bottom:30px;
    left:30px;
    right:30px;
}

.hero-card-content h3{
    font-family:"Manrope";
    font-size:30px;
    margin-bottom:10px;
}

.hero-card-content p{
    font-size:14px;
    line-height:1.6;
    color:var(--muted);
}

.country-row{
    display:flex;
    gap:10px;
    margin-top:20px;
}

.country{
    border:1px solid var(--border);
    padding:8px 12px;
    border-radius:10px;
    font-size:12px;
    font-weight:700;
    background:rgba(255,255,255,.05);
}

/* GENERAL */

section{
    max-width:1180px;
    margin:auto;
    padding:110px 25px;
}

.section-head{
    max-width:720px;
    margin-bottom:50px;
}

.eyebrow{
    color:var(--cyan);
    text-transform:uppercase;
    font-size:11px;
    letter-spacing:2px;
    font-weight:800;
    margin-bottom:13px;
}

.section-head h2{
    font-family:"Manrope";
    font-size:clamp(35px,5vw,58px);
    letter-spacing:-2.5px;
    line-height:1;
}

.section-head p{
    color:var(--muted);
    line-height:1.7;
    margin-top:18px;
}

/* ABOUT */

.about-grid{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:20px;
}

.about-main,
.info-card{
    border:1px solid var(--border);
    background:var(--card);
    border-radius:25px;
    padding:30px;
}

.about-main{
    min-height:320px;
}

.about-main h3{
    font-family:"Manrope";
    font-size:28px;
    margin-bottom:18px;
}

.about-main p{
    color:var(--muted);
    line-height:1.8;
}

.about-main button{
    margin-top:25px;
}

.info-grid{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:20px;
}

.info-card{
    cursor:pointer;
    transition:.3s;
}

.info-card:hover{
    transform:translateY(-5px);
    background:var(--card2);
    border-color:rgba(91,140,255,.5);
}

.icon{
    width:44px;
    height:44px;
    display:grid;
    place-items:center;
    border-radius:13px;
    background:rgba(91,140,255,.12);
    margin-bottom:20px;
    font-size:20px;
}

.info-card h4{
    margin-bottom:8px;
}

.info-card p{
    color:var(--muted);
    font-size:13px;
    line-height:1.6;
}

/* PLACES */

.places{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:18px;
}

.place{
    position:relative;
    overflow:hidden;
    min-height:280px;
    padding:25px;
    border:1px solid var(--border);
    background:linear-gradient(145deg,rgba(255,255,255,.075),rgba(255,255,255,.025));
    border-radius:25px;
    cursor:pointer;
    transition:.35s;
}

.place:hover{
    transform:translateY(-7px);
    border-color:rgba(66,217,255,.4);
    box-shadow:0 20px 60px rgba(0,0,0,.25);
}

.place-number{
    color:#65708b;
    font-size:11px;
    font-weight:800;
    letter-spacing:2px;
}

.place h3{
    position:absolute;
    bottom:55px;
    left:25px;
    font-family:"Manrope";
    font-size:25px;
}

.place p{
    position:absolute;
    bottom:25px;
    left:25px;
    color:var(--muted);
    font-size:12px;
}

.place-glow{
    position:absolute;
    width:150px;
    height:150px;
    border-radius:50%;
    filter:blur(55px);
    opacity:.18;
    right:-50px;
    top:-50px;
}

.glow-blue{background:var(--blue)}
.glow-purple{background:var(--purple)}
.glow-cyan{background:var(--cyan)}
.glow-pink{background:var(--pink)}
.glow-green{background:var(--green)}
.glow-yellow{background:var(--yellow)}

/* EXCHANGE */

.exchange-section{
    max-width:none;
    background:
        radial-gradient(circle at 10% 30%,rgba(91,140,255,.12),transparent 30%),
        radial-gradient(circle at 90% 70%,rgba(155,108,255,.12),transparent 30%),
        #0a1021;
    border-top:1px solid var(--border);
    border-bottom:1px solid var(--border);
}

.exchange-inner{
    max-width:1180px;
    margin:auto;
    padding:110px 25px;
}

.exchange-grid{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:20px;
}

.exchange-card{
    padding:40px;
    border:1px solid var(--border);
    border-radius:28px;
    background:rgba(255,255,255,.045);
    cursor:pointer;
    transition:.3s;
}

.exchange-card:hover{
    transform:translateY(-5px);
    background:rgba(255,255,255,.075);
}

.exchange-card .flag{
    font-size:40px;
    margin-bottom:25px;
}

.exchange-card h3{
    font-family:"Manrope";
    font-size:28px;
    margin-bottom:15px;
}

.exchange-card p{
    color:var(--muted);
    line-height:1.7;
}

.exchange-card ul{
    margin-top:20px;
    list-style:none;
}

.exchange-card li{
    padding:10px 0;
    color:#c5cce0;
    border-bottom:1px solid rgba(255,255,255,.07);
    font-size:14px;
}

.exchange-card li::before{
    content:"✓";
    color:var(--green);
    margin-right:10px;
}

/* PROGRAMME */

.programme{
    display:grid;
    gap:12px;
}

.day{
    border:1px solid var(--border);
    background:var(--card);
    border-radius:20px;
    padding:25px;
    display:grid;
    grid-template-columns:90px 1fr 40px;
    align-items:center;
    cursor:pointer;
    transition:.25s;
}

.day:hover{
    background:var(--card2);
    border-color:rgba(91,140,255,.4);
    transform:translateX(5px);
}

.day-number{
    color:var(--blue);
    font-size:12px;
    font-weight:800;
}

.day h3{
    font-size:18px;
}

.day p{
    color:var(--muted);
    margin-top:5px;
    font-size:13px;
}

.arrow{
    font-size:22px;
    color:#8792ad;
}

/* PRICING */

.pricing-section{
    background:linear-gradient(
        180deg,
        transparent,
        rgba(91,140,255,.045),
        transparent
    );
}

.pricing{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:18px;
}

.price-card{
    border:1px solid var(--border);
    background:var(--card);
    border-radius:28px;
    padding:32px;
    position:relative;
    transition:.3s;
    cursor:pointer;
}

.price-card:hover{
    transform:translateY(-7px);
    border-color:rgba(155,108,255,.5);
}

.price-card.featured{
    background:
        linear-gradient(145deg,rgba(91,140,255,.15),rgba(155,108,255,.1)),
        var(--card);
    border-color:rgba(91,140,255,.45);
}

.popular{
    position:absolute;
    right:20px;
    top:20px;
    background:linear-gradient(90deg,var(--blue),var(--purple));
    padding:6px 10px;
    border-radius:8px;
    font-size:9px;
    font-weight:800;
}

.price-card h3{
    font-size:20px;
}

.price{
    font-family:"Manrope";
    font-size:48px;
    font-weight:800;
    margin:20px 0 5px;
}

.per{
    color:var(--muted);
    font-size:12px;
}

.price-card > p{
    color:var(--muted);
    line-height:1.6;
    font-size:13px;
    margin:20px 0;
}

.price-list{
    list-style:none;
}

.price-list li{
    padding:11px 0;
    border-bottom:1px solid rgba(255,255,255,.07);
    color:#c6cee1;
    font-size:13px;
}

.price-list li::before{
    content:"✓";
    color:var(--green);
    margin-right:9px;
}

/* CULTURE */

.culture-grid{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:20px;
}

.culture{
    min-height:340px;
    border:1px solid var(--border);
    border-radius:28px;
    padding:35px;
    background:var(--card);
    cursor:pointer;
    transition:.3s;
}

.culture:hover{
    transform:translateY(-6px);
    background:var(--card2);
}

.culture .big{
    font-size:55px;
}

.culture h3{
    font-family:"Manrope";
    font-size:28px;
    margin:25px 0 12px;
}

.culture p{
    color:var(--muted);
    line-height:1.7;
}

/* FAQ */

.faq{
    display:grid;
    gap:12px;
}

.faq-item{
    border:1px solid var(--border);
    border-radius:18px;
    background:var(--card);
    overflow:hidden;
}

.faq-question{
    padding:23px;
    display:flex;
    justify-content:space-between;
    align-items:center;
    cursor:pointer;
    font-weight:700;
}

.faq-answer{
    max-height:0;
    overflow:hidden;
    transition:.35s;
}

.faq-answer p{
    padding:0 23px 23px;
    color:var(--muted);
    line-height:1.7;
    font-size:14px;
}

.faq-item.active .faq-answer{
    max-height:300px;
}

.faq-item.active .plus{
    transform:rotate(45deg);
}

/* CTA */

.cta{
    max-width:1130px;
    margin:50px auto 100px;
    padding:70px 40px;
    text-align:center;
    border-radius:35px;
    border:1px solid var(--border);
    background:
        radial-gradient(circle at 50% 0%,rgba(91,140,255,.2),transparent 45%),
        rgba(255,255,255,.04);
}

.cta h2{
    font-family:"Manrope";
    font-size:clamp(38px,5vw,65px);
    letter-spacing:-3px;
}

.cta p{
    color:var(--muted);
    max-width:600px;
    margin:20px auto 30px;
    line-height:1.7;
}

/* FOOTER */

footer{
    border-top:1px solid var(--border);
    padding:35px 25px;
    color:#65708b;
    font-size:12px;
}

.footer-inner{
    max-width:1180px;
    margin:auto;
    display:flex;
    justify-content:space-between;
    gap:20px;
}

/* MODAL */

.modal{
    position:fixed;
    inset:0;
    background:rgba(2,5,15,.82);
    backdrop-filter:blur(15px);
    z-index:2000;
    display:none;
    align-items:center;
    justify-content:center;
    padding:20px;
}

.modal.show{
    display:flex;
}

.modal-box{
    width:min(720px,100%);
    max-height:85vh;
    overflow-y:auto;
    border:1px solid var(--border);
    background:
        radial-gradient(circle at 100% 0%,rgba(155,108,255,.15),transparent 35%),
        #0d1429;
    border-radius:30px;
    padding:35px;
    box-shadow:0 40px 100px rgba(0,0,0,.5);
    animation:modalIn .25s ease;
}

@keyframes modalIn{
    from{
        opacity:0;
        transform:translateY(20px) scale(.97);
    }
    to{
        opacity:1;
        transform:none;
    }
}

.modal-top{
    display:flex;
    justify-content:space-between;
    align-items:start;
}

.modal-label{
    color:var(--cyan);
    text-transform:uppercase;
    letter-spacing:2px;
    font-size:10px;
    font-weight:800;
}

.modal h2{
    font-family:"Manrope";
    font-size:36px;
    margin-top:8px;
}

.close{
    width:38px;
    height:38px;
    border-radius:12px;
    border:1px solid var(--border);
    background:rgba(255,255,255,.05);
    color:white;
    cursor:pointer;
    font-size:20px;
}

.modal-description{
    color:var(--muted);
    line-height:1.8;
    margin-top:22px;
}

.modal-list{
    margin-top:25px;
    display:grid;
    gap:10px;
}

.modal-list div{
    padding:15px;
    border:1px solid rgba(255,255,255,.08);
    border-radius:13px;
    background:rgba(255,255,255,.035);
    color:#cdd4e7;
    font-size:14px;
}

.modal-list div::before{
    content:"✦";
    color:var(--cyan);
    margin-right:10px;
}

/* MOBILE */

@media(max-width:950px){

    .navlinks{
        display:none;
    }

    .hero{
        grid-template-columns:1fr;
        padding-top:140px;
    }

    .hero-card{
        min-height:380px;
    }

    .places{
        grid-template-columns:1fr 1fr;
    }

    .pricing{
        grid-template-columns:1fr;
    }

}

@media(max-width:650px){

    nav{
        top:10px;
    }

    .nav-button{
        display:none;
    }

    section{
        padding:80px 18px;
    }

    .hero{
        padding:130px 18px 70px;
    }

    .hero h1{
        letter-spacing:-3px;
    }

    .hero p{
        font-size:15px;
    }

    .about-grid,
    .info-grid,
    .exchange-grid,
    .culture-grid,
    .places{
        grid-template-columns:1fr;
    }

    .day{
        grid-template-columns:60px 1fr 25px;
    }

    .modal-box{
        padding:25px;
    }

    .modal h2{
        font-size:29px;
    }

    .footer-inner{
        flex-direction:column;
    }

}

</style>
</head>

<body>

<!-- NAVIGATION -->

<nav>

    <div class="logo">
        WAŁBRZYCH<span>+</span>
    </div>

    <div class="navlinks">
        <a href="#about">About</a>
        <a href="#places">Explore</a>
        <a href="#exchange">Exchange</a>
        <a href="#programme">Programme</a>
        <a href="#pricing">Pricing</a>
        <a href="#faq">FAQ</a>
    </div>

    <button class="nav-button"
        onclick="openModal(
        'Join the Exchange',
        'START HERE',
        'The Polish × English Student Exchange is designed to connect students, schools and cultures through an educational experience in Wałbrzych.',
        [
        'Meet students from another country',
        'Explore Wałbrzych and Lower Silesia',
        'Take part in school activities',
        'Practice English in real situations',
        'Discover Polish culture and traditions'
        ])">
        Join us →
    </button>

</nav>


<!-- HERO -->

<header class="hero">

    <div>

        <div class="badge">
            <span class="badge-dot"></span>
            POLAND × ENGLAND · STUDENT EXCHANGE 2026
        </div>

        <h1>
            Discover
            <span class="gradient">Wałbrzych.</span>
        </h1>

        <p>
            A modern Polish–English student exchange built around
            friendship, education, culture and discovering one of
            Lower Silesia's most interesting cities.
        </p>

        <div class="hero-buttons">

            <a href="#places" class="primary">
                Explore Wałbrzych →
            </a>

            <a href="#pricing" class="secondary">
                View pricing
            </a>

        </div>

    </div>


    <div class="hero-card">

        <div class="hero-card-top">

            <div class="small-label">
                INTERNATIONAL PROGRAMME
            </div>

            <div class="year">
                2026
            </div>

        </div>

        <div class="globe"></div>

        <div class="hero-card-content">

            <h3>
                Poland × England
            </h3>

            <p>
                One week. Two cultures. New friendships,
                new experiences and a completely different
                way to learn.
            </p>

            <div class="country-row">

                <div class="country">
                    🇵🇱 Poland
                </div>

                <div class="country">
                    🇬🇧 England
                </div>

            </div>

        </div>

    </div>

</header>


<!-- ABOUT -->

<section id="about">

    <div class="section-head">

        <div class="eyebrow">
            01 · About
        </div>

        <h2>
            More than a school trip.
        </h2>

        <p>
            The exchange combines education, travel and international
            friendship into one experience.
        </p>

    </div>


    <div class="about-grid">

        <div class="about-main">

            <h3>
                Why Wałbrzych?
            </h3>

            <p>
                Wałbrzych is located in Lower Silesia, surrounded by
                mountains, forests and historic architecture. The city
                combines industrial heritage with cultural attractions
                and beautiful natural landscapes.
            </p>

            <p style="margin-top:15px;">
                For students, this creates an ideal environment to learn
                outside the classroom, discover another culture and
                communicate in English every day.
            </p>

            <button class="primary"
                onclick="openModal(
                'Why Wałbrzych?',
                'THE CITY',
                'Wałbrzych offers a combination of history, nature, architecture and modern student activities. It is large enough to have many attractions while still being easy to explore during a short exchange.',
                [
                'Historic Książ Castle',
                'Chełmiec mountain and surrounding trails',
                'Palm House and botanical collections',
                'Historic city centre',
                'Museums and cultural institutions',
                'Easy access to other Lower Silesian destinations'
                ])">
                Discover the city
            </button>

        </div>


        <div class="info-grid">

            <div class="info-card"
                onclick="openModal(
                'Location',
                '01',
                'Wałbrzych is a city in south-western Poland, in Lower Silesia. Its location makes it a useful starting point for exploring the surrounding region.',
                [
                'South-western Poland',
                'Lower Silesia',
                'Mountain landscapes nearby',
                'Historic towns and attractions in the region'
                ])">

                <div class="icon">📍</div>

                <h4>Location</h4>

                <p>
                    Discover where Wałbrzych is and what surrounds it.
                </p>

            </div>


            <div class="info-card"
                onclick="openModal(
                'Education',
                '02',
                'The exchange gives students opportunities to learn through real-life situations rather than only traditional classroom exercises.',
                [
                'International teamwork',
                'English communication',
                'School visits',
                'Presentations',
                'Cultural workshops'
                ])">

                <div class="icon">🎓</div>

                <h4>Education</h4>

                <p>
                    Learning through international experience.
                </p>

            </div>


            <div class="info-card"
                onclick="openModal(
                'Friendship',
                '03',
                'Meeting students from another country can help participants build confidence and create friendships that continue after the exchange.',
                [
                'Meet international students',
                'Work together in groups',
                'Share hobbies and interests',
                'Communicate outside school',
                'Keep in touch after the trip'
                ])">

                <div class="icon">🤝</div>

                <h4>Friendship</h4>

                <p>
                    Connect with people from another country.
                </p>

            </div>


            <div class="info-card"
                onclick="openModal(
                'Experience',
                '04',
                'The exchange is designed to be memorable. Students experience school, culture, sightseeing and everyday life in a different environment.',
                [
                'City exploration',
                'Cultural activities',
                'Local food',
                'Outdoor activities',
                'Group challenges',
                'Free time with new friends'
                ])">

                <div class="icon">✨</div>

                <h4>Experience</h4>

                <p>
                    A week full of new experiences.
                </p>

            </div>

        </div>

    </div>

</section>


<!-- PLACES -->

<section id="places">

    <div class="section-head">

        <div class="eyebrow">
            02 · Explore
        </div>

        <h2>
            Places worth discovering.
        </h2>

        <p>
            Click any destination to see a detailed description
            and ideas for activities.
        </p>

    </div>


    <div class="places">

        <div class="place"
            onclick="openModal(
            'Książ Castle',
            'DESTINATION 01',
            'Książ Castle is one of the most famous landmarks of Lower Silesia. Its historic architecture, large grounds and surrounding landscape make it a perfect destination for a student excursion.',
            [
            'Explore the castle interiors',
            'Discover its history and legends',
            'Walk through the surrounding gardens',
            'Visit the nearby Palm House',
            'Take photographs and create a student travel journal',
            'Learn about the region through architecture'
            ])">

            <span class="place-number">01</span>

            <div class="place-glow glow-blue"></div>

            <h3>Książ Castle</h3>

            <p>History · Architecture · Gardens</p>

        </div>


        <div class="place"
            onclick="openModal(
            'Chełmiec',
            'DESTINATION 02',
            'Chełmiec is one of the most recognizable mountains around Wałbrzych. The area offers opportunities for walking, observing nature and enjoying views over the region.',
            [
            'Mountain walk',
            'Nature observation',
            'Photography challenge',
            'Team activities',
            'Learn about the local landscape',
            'Enjoy panoramic views'
            ])">

            <span class="place-number">02</span>

            <div class="place-glow glow-green"></div>

            <h3>Chełmiec</h3>

            <p>Nature · Mountains · Adventure</p>

        </div>


        <div class="place"
            onclick="openModal(
            'Old Wałbrzych',
            'DESTINATION 03',
            'The historic parts of Wałbrzych show how the city developed over time. Students can explore streets, buildings and public spaces while learning about local history.',
            [
            'Historic architecture',
            'City walking tour',
            'Local history',
            'Photography route',
            'Urban exploration',
            'Group quiz'
            ])">

            <span class="place-number">03</span>

            <div class="place-glow glow-purple"></div>

            <h3>Old Wałbrzych</h3>

            <p>History · Streets · Architecture</p>

        </div>


        <div class="place"
            onclick="openModal(
            'Palm House',
            'DESTINATION 04',
            'The Palm House is a botanical attraction connected with Książ. It provides a completely different environment from the surrounding mountain landscape.',
            [
            'Explore tropical plants',
            'Learn about exotic species',
            'Botanical photography',
            'Educational activities',
            'Discover the history of the Palm House'
            ])">

            <span class="place-number">04</span>

            <div class="place-glow glow-cyan"></div>

            <h3>Palm House</h3>

            <p>Nature · Plants · Education</p>

        </div>


        <div class="place"
            onclick="openModal(
            'Culture & Museums',
            'DESTINATION 05',
            'Wałbrzych has cultural institutions where students can learn about local history, art and the development of the city.',
            [
            'Museums',
            'Cultural events',
            'Local history',
            'Art and exhibitions',
            'Student workshops',
            'Creative projects'
            ])">

            <span class="place-number">05</span>

            <div class="place-glow glow-pink"></div>

            <h3>Culture</h3>

            <p>Art · Museums · History</p>

        </div>


        <div class="place"
            onclick="openModal(
            'Lower Silesia',
            'DESTINATION 06',
            'Wałbrzych can also be used as a base for discovering other places in Lower Silesia. The region has castles, mountains, historic towns and cultural attractions.',
            [
            'Regional excursions',
            'Historic towns',
            'Mountain landscapes',
            'Castles and palaces',
            'Local traditions',
            'Regional food'
            ])">

            <span class="place-number">06</span>

            <div class="place-glow glow-yellow"></div>

            <h3>Lower Silesia</h3>

            <p>Region · Travel · Discovery</p>

        </div>

    </div>

</section>


<!-- EXCHANGE -->

<div class="exchange-section" id="exchange">

    <div class="exchange-inner">

        <div class="section-head">

            <div class="eyebrow">
                03 · Exchange
            </div>

            <h2>
                Two countries.
                One experience.
            </h2>

            <p>
                Students from Poland and England learn from each other
                and experience everyday life from a new perspective.
            </p>

        </div>


        <div class="exchange-grid">

            <div class="exchange-card"
                onclick="openModal(
                'Polish Students',
                '🇵🇱 POLAND',
                'Polish students become local hosts and guides. They can introduce their international partners to Wałbrzych, Polish school life and local traditions.',
                [
                'Introduce your city',
                'Practice English every day',
                'Show Polish traditions',
                'Work in international teams',
                'Help international visitors feel welcome',
                'Share your favourite places'
                ])">

                <div class="flag">🇵🇱</div>

                <h3>Polish Students</h3>

                <p>
                    Become a guide, host and cultural ambassador
                    for your city.
                </p>

                <ul>
                    <li>Local knowledge</li>
                    <li>English practice</li>
                    <li>International teamwork</li>
                    <li>Cultural exchange</li>
                </ul>

            </div>


            <div class="exchange-card"
                onclick="openModal(
                'English Students',
                '🇬🇧 ENGLAND',
                'English students can discover Polish culture directly by spending time with local students, visiting schools and exploring Wałbrzych.',
                [
                'Discover Polish school life',
                'Explore Wałbrzych',
                'Practice communication',
                'Learn about Polish traditions',
                'Try local food',
                'Create international friendships'
                ])">

                <div class="flag">🇬🇧</div>

                <h3>English Students</h3>

                <p>
                    Discover Poland through real experiences
                    instead of only reading about it.
                </p>

                <ul>
                    <li>Explore local culture</li>
                    <li>Visit Polish schools</li>
                    <li>Meet local students</li>
                    <li>Discover the region</li>
                </ul>

            </div>

        </div>

    </div>

</div>


<!-- PROGRAMME -->

<section id="programme">

    <div class="section-head">

        <div class="eyebrow">
            04 · Programme
        </div>

        <h2>
            A week designed to remember.
        </h2>

        <p>
            Click each day to see what students can experience.
        </p>

    </div>


    <div class="programme">

        <div class="day"
            onclick="openModal(
            'Arrival Day',
            'DAY 01 · ARRIVAL',
            'The first day is about meeting everyone, settling in and getting comfortable in a new environment.',
            [
            'Arrival in Wałbrzych',
            'Welcome meeting',
            'Introduction to the exchange',
            'Meet your partner student',
            'Safety and programme briefing',
            'Welcome dinner or group activity'
            ])">

            <div class="day-number">DAY 01</div>

            <div>
                <h3>Arrival & Welcome</h3>
                <p>First meeting, introductions and getting settled.</p>
            </div>

            <div class="arrow">→</div>

        </div>


        <div class="day"
            onclick="openModal(
            'School Day',
            'DAY 02 · EDUCATION',
            'Students spend part of the day at school and participate in activities designed to encourage international communication.',
            [
            'School tour',
            'Meet teachers and students',
            'International group project',
            'English communication activities',
            'Lunch together',
            'Afternoon free time'
            ])">

            <div class="day-number">DAY 02</div>

            <div>
                <h3>School & Teamwork</h3>
                <p>Education, workshops and international projects.</p>
            </div>

            <div class="arrow">→</div>

        </div>


        <div class="day"
            onclick="openModal(
            'Książ Day',
            'DAY 03 · EXPLORATION',
            'A full day focused on one of the region’s most famous attractions and its history.',
            [
            'Travel to Książ',
            'Castle exploration',
            'History activity',
            'Group photography challenge',
            'Visit to the Palm House',
            'Reflection and group discussion'
            ])">

            <div class="day-number">DAY 03</div>

            <div>
                <h3>Książ Castle</h3>
                <p>History, architecture and regional exploration.</p>
            </div>

            <div class="arrow">→</div>

        </div>


        <div class="day"
            onclick="openModal(
            'Culture Day',
            'DAY 04 · CULTURE',
            'Students compare Polish and English culture through food, traditions, language and everyday life.',
            [
            'Polish culture workshop',
            'English culture presentation',
            'Traditional food tasting',
            'Music and entertainment',
            'International quiz',
            'Student presentations'
            ])">

            <div class="day-number">DAY 04</div>

            <div>
                <h3>Culture Exchange</h3>
                <p>Food, traditions, language and stories.</p>
            </div>

            <div class="arrow">→</div>

        </div>


        <div class="day"
            onclick="openModal(
            'Adventure Day',
            'DAY 05 · OUTDOORS',
            'Students spend time outside and discover the natural landscape around Wałbrzych.',
            [
            'Outdoor walk',
            'Nature observation',
            'Team challenges',
            'Photography',
            'Free time',
            'Group picnic or meeting'
            ])">

            <div class="day-number">DAY 05</div>

            <div>
                <h3>Nature & Adventure</h3>
                <p>Mountains, nature and teamwork.</p>
            </div>

            <div class="arrow">→</div>

        </div>

    </div>

</section>


<!-- PRICING -->

<section id="pricing" class="pricing-section">

    <div class="section-head">

        <div class="eyebrow">
            05 · Pricing
        </div>

        <h2>
            Choose your experience.
        </h2>

        <p>
            Click a package to see exactly what can be included.
        </p>

    </div>


    <div class="pricing">


        <div class="price-card"
            onclick="openModal(
            'Basic Package',
            '€120 · PER STUDENT',
            'A simple option for students who want to participate in the core exchange programme.',
            [
            'Welcome and orientation',
            'School activities',
            'Basic cultural programme',
            'Selected group activities',
            'Exchange materials',
            'Student certificate'
            ])">

            <h3>Basic</h3>

            <div class="price">€120</div>

            <div class="per">per student</div>

            <p>
                Essential exchange activities
                and educational programme.
            </p>

            <ul class="price-list">
                <li>School programme</li>
                <li>Welcome activities</li>
                <li>Cultural workshop</li>
                <li>Certificate</li>
            </ul>

        </div>


        <div class="price-card featured"
            onclick="openModal(
            'Standard Package',
            '€250 · PER STUDENT',
            'A balanced package combining education, sightseeing and cultural activities. It is designed as a complete exchange experience.',
            [
            'Everything in Basic',
            'Książ Castle visit',
            'Palm House visit',
            'Additional cultural activities',
            'Guided city exploration',
            'Group project',
            'Exchange merchandise',
            'Additional programme materials'
            ])">

            <div class="popular">
                MOST COMPLETE
            </div>

            <h3>Standard</h3>

            <div class="price">€250</div>

            <div class="per">per student</div>

            <p>
                A complete balance of school,
                culture and sightseeing.
            </p>

            <ul class="price-list">
                <li>Everything in Basic</li>
                <li>Książ Castle</li>
                <li>Palm House</li>
                <li>City tour</li>
                <li>Cultural activities</li>
                <li>Student project</li>
            </ul>

        </div>


        <div class="price-card"
            onclick="openModal(
            'Premium Package',
            '€390 · PER STUDENT',
            'An extended package for students who want to experience more of Wałbrzych and Lower Silesia.',
            [
            'Everything in Standard',
            'Extended regional excursion',
            'Additional outdoor activity',
            'Extra cultural workshop',
            'Additional guided tour',
            'Premium exchange materials',
            'Special closing event',
            'Commemorative package'
            ])">

            <h3>Premium</h3>

            <div class="price">€390</div>

            <div class="per">per student</div>

            <p>
                An extended programme with
                additional activities.
            </p>

            <ul class="price-list">
                <li>Everything in Standard</li>
                <li>Regional excursion</li>
                <li>Outdoor activity</li>
                <li>Extra workshops</li>
                <li>Closing event</li>
            </ul>

        </div>

    </div>

</section>


<!-- CULTURE -->

<section>

    <div class="section-head">

        <div class="eyebrow">
            06 · Culture
        </div>

        <h2>
            Two cultures. Endless things to share.
        </h2>

        <p>
            Click a country to discover some of the cultural themes
            students can explore together.
        </p>

    </div>


    <div class="culture-grid">


        <div class="culture"
            onclick="openModal(
            'Polish Culture',
            '🇵🇱 POLAND',
            'Polish students can introduce their international partners to traditions, food, celebrations, music, school life and everyday customs.',
            [
            'Polish traditional food',
            'Christmas and Easter traditions',
            'Polish school life',
            'Local history',
            'Polish music',
            'Language and useful expressions',
            'Family and social traditions'
            ])">

            <div class="big">🇵🇱</div>

            <h3>Polish Culture</h3>

            <p>
                Discover Polish traditions, food, history,
                school life and everyday customs.
            </p>

        </div>


        <div class="culture"
            onclick="openModal(
            'English Culture',
            '🇬🇧 ENGLAND',
            'English students can share traditions and everyday experiences from England and compare them with Polish culture.',
            [
            'British school life',
            'Traditional food',
            'Music and entertainment',
            'Sports culture',
            'British celebrations',
            'English expressions',
            'Everyday life in England'
            ])">

            <div class="big">🇬🇧</div>

            <h3>English Culture</h3>

            <p>
                Explore British traditions, language,
                school life and everyday experiences.
            </p>

        </div>

    </div>

</section>


<!-- FAQ -->

<section id="faq">

    <div class="section-head">

        <div class="eyebrow">
            07 · FAQ
        </div>

        <h2>
            Questions, answered.
        </h2>

    </div>


    <div class="faq">


        <div class="faq-item">

            <div class="faq-question"
                onclick="toggleFAQ(this)">

                <span>
                    Who can participate in the exchange?
                </span>

                <span class="plus">+</span>

            </div>

            <div class="faq-answer">

                <p>
                    The programme is designed for school students
                    participating through partner schools in Poland
                    and England. The exact age group and number of
                    participants can be decided by the schools.
                </p>

            </div>

        </div>


        <div class="faq-item">

            <div class="faq-question"
                onclick="toggleFAQ(this)">

                <span>
                    Do I need to speak perfect English?
                </span>

                <span class="plus">+</span>

            </div>

            <div class="faq-answer">

                <p>
                    No. The exchange is also an opportunity to practise
                    English. Students can communicate using simple
                    language, gestures, translation tools and help from
                    teachers when necessary.
                </p>

            </div>

        </div>


        <div class="faq-item">

            <div class="faq-question"
                onclick="toggleFAQ(this)">

                <span>
                    What will students do after school?
                </span>

                <span class="plus">+</span>

            </div>

            <div class="faq-answer">

                <p>
                    Afternoon activities can include sightseeing,
                    cultural workshops, group projects, outdoor
                    activities, free time and meeting with partner
                    students.
                </p>

            </div>

        </div>


        <div class="faq-item">

            <div class="faq-question"
                onclick="toggleFAQ(this)">

                <span>
                    Can students stay with host families?
                </span>

                <span class="plus">+</span>

            </div>

            <div class="faq-answer">

                <p>
                    Depending on the organisation of the exchange,
                    students may stay with carefully selected host
                    families or use another accommodation arranged
                    by the participating schools.
                </p>

            </div>

        </div>


        <div class="faq-item">

            <div class="faq-question"
                onclick="toggleFAQ(this)">

                <span>
                    What is the main goal of the exchange?
                </span>

                <span class="plus">+</span>

            </div>

            <div class="faq-answer">

                <p>
                    The main goal is to combine education with
                    international communication. Students can practise
                    languages, learn about another culture, develop
                    independence and create international friendships.
                </p>

            </div>

        </div>

    </div>

</section>


<!-- CTA -->

<div class="cta">

    <div class="eyebrow">
        READY?
    </div>

    <h2>
        Your exchange
        <span class="gradient">starts here.</span>
    </h2>

    <p>
        Discover Wałbrzych, meet new people, practise English
        and experience Poland from a completely new perspective.
    </p>

    <button class="primary"
        onclick="openModal(
        'Welcome to Wałbrzych',
        'POLAND × ENGLAND',
        'The student exchange is about more than travelling. It is about meeting people, discovering a new culture and creating memories together.',
        [
        'Explore Wałbrzych',
        'Meet international students',
        'Learn outside the classroom',
        'Share your culture',
        'Create memories together'
        ])">

        Start the journey →

    </button>

</div>


<!-- FOOTER -->

<footer>

    <div class="footer-inner">

        <div>
            WAŁBRZYCH+ · POLISH × ENGLISH STUDENT EXCHANGE
        </div>

        <div>
            Discover · Learn · Connect · 2026
        </div>

    </div>

</footer>


<!-- MODAL -->

<div class="modal" id="modal">

    <div class="modal-box">

        <div class="modal-top">

            <div>

                <div class="modal-label" id="modalLabel">
                    INFORMATION
                </div>

                <h2 id="modalTitle">
                    Title
                </h2>

            </div>

            <button class="close"
                onclick="closeModal()">
                ×
            </button>

        </div>


        <p class="modal-description"
            id="modalDescription">
        </p>


        <div class="modal-list"
            id="modalList">
        </div>

    </div>

</div>


<script>

/* MODAL */

function openModal(title,label,text,items){

    document.getElementById("modalTitle").textContent = title;

    document.getElementById("modalLabel").textContent = label;

    document.getElementById("modalDescription").textContent = text;

    const list = document.getElementById("modalList");

    list.innerHTML = "";

    items.forEach(item => {

        const div = document.createElement("div");

        div.textContent = item;

        list.appendChild(div);

    });

    document.getElementById("modal").classList.add("show");

    document.body.style.overflow = "hidden";
}


function closeModal(){

    document.getElementById("modal").classList.remove("show");

    document.body.style.overflow = "";

}


document.getElementById("modal").addEventListener("click",function(e){

    if(e.target === this){

        closeModal();

    }

});


document.addEventListener("keydown",function(e){

    if(e.key === "Escape"){

        closeModal();

    }

});


/* FAQ */

function toggleFAQ(element){

    const item = element.parentElement;

    const all = document.querySelectorAll(".faq-item");

    all.forEach(other => {

        if(other !== item){

            other.classList.remove("active");

        }

    });

    item.classList.toggle("active");

}


/* NAVIGATION SHADOW */

window.addEventListener("scroll",function(){

    const nav = document.querySelector("nav");

    if(window.scrollY > 30){

        nav.style.boxShadow =
        "0 15px 50px rgba(0,0,0,.35)";

    }else{

        nav.style.boxShadow = "none";

    }

});


/* CLOSE MODAL WITH ESC */

document.addEventListener("keydown",function(e){

    if(e.key === "Escape"){

        closeModal();

    }

});


/* REVEAL ANIMATION */

const observer = new IntersectionObserver(

    entries => {

        entries.forEach(entry => {

            if(entry.isIntersecting){

                entry.target.style.opacity = "1";

                entry.target.style.transform = "translateY(0)";

            }

        });

    },

    {threshold:.08}

);


document.querySelectorAll(
    ".place, .info-card, .exchange-card, .day, .price-card, .culture"
).forEach(el => {

    el.style.opacity = "0";

    el.style.transform = "translateY(20px)";

    el.style.transition =
        "opacity .6s ease, transform .6s ease";

    observer.observe(el);

});


</script>

</body>
</html>
