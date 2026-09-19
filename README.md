```html
<!DOCTYPE html>
<html lang="mk">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Автоперална Торнадо</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    scroll-behavior:smooth;
}

body{
    font-family:Arial, Helvetica, sans-serif;
    background:#08090b;
    color:white;
}

header{
    position:fixed;
    top:0;
    left:0;
    width:100%;
    z-index:1000;
    background:rgba(8,9,11,.9);
    backdrop-filter:blur(12px);
    border-bottom:1px solid rgba(255,255,255,.08);
}

.nav{
    max-width:1200px;
    margin:auto;
    height:80px;
    display:flex;
    align-items:center;
    justify-content:space-between;
    padding:0 20px;
}

.logo{
    font-size:25px;
    font-weight:900;
    letter-spacing:2px;
}

.logo span{
    color:#00aaff;
}

nav{
    display:flex;
    gap:28px;
}

nav a{
    color:white;
    text-decoration:none;
    font-weight:bold;
    transition:.3s;
}

nav a:hover{
    color:#00aaff;
}

.menu{
    display:none;
    font-size:30px;
    cursor:pointer;
}

.hero{
    min-height:100vh;
    display:flex;
    align-items:center;
    justify-content:center;
    text-align:center;
    padding:120px 20px 60px;
    background:
        radial-gradient(circle at 50% 30%,rgba(0,170,255,.18),transparent 35%),
        linear-gradient(135deg,#08090b,#10141a);
    position:relative;
    overflow:hidden;
}

.hero:before{
    content:"";
    position:absolute;
    width:500px;
    height:500px;
    border:1px solid rgba(0,170,255,.12);
    border-radius:50%;
    animation:rotate 15s linear infinite;
}

.hero-content{
    position:relative;
    z-index:2;
    max-width:850px;
}

.badge{
    display:inline-block;
    padding:9px 18px;
    border:1px solid rgba(0,170,255,.5);
    border-radius:30px;
    color:#00aaff;
    margin-bottom:20px;
    font-size:14px;
}

h1{
    font-size:clamp(48px,8vw,90px);
    line-height:.95;
    font-weight:900;
}

h1 span{
    color:#00aaff;
}

.hero p{
    margin:25px auto;
    max-width:650px;
    color:#b9bec7;
    font-size:18px;
    line-height:1.7;
}

.buttons{
    display:flex;
    justify-content:center;
    gap:15px;
    flex-wrap:wrap;
}

.btn{
    padding:15px 28px;
    border-radius:10px;
    text-decoration:none;
    font-weight:bold;
    transition:.3s;
    display:inline-block;
}

.btn-primary{
    background:#00aaff;
    color:#001018;
}

.btn-primary:hover{
    transform:translateY(-4px);
    box-shadow:0 10px 30px rgba(0,170,255,.3);
}

.btn-secondary{
    border:1px solid #30353d;
    color:white;
}

.btn-secondary:hover{
    border-color:#00aaff;
    color:#00aaff;
}

section{
    padding:100px 20px;
}

.container{
    max-width:1200px;
    margin:auto;
}

.section-title{
    text-align:center;
    margin-bottom:55px;
}

.section-title h2{
    font-size:42px;
    margin-bottom:12px;
}

.section-title h2 span{
    color:#00aaff;
}

.section-title p{
    color:#969ca5;
}

.services{
    background:#0c0e12;
}

.cards{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:22px;
}

.card{
    background:#111419;
    border:1px solid #20252d;
    border-radius:18px;
    padding:32px;
    transition:.35s;
}

.card:hover{
    transform:translateY(-8px);
    border-color:#00aaff;
    box-shadow:0 15px 40px rgba(0,0,0,.3);
}

.icon{
    width:58px;
    height:58px;
    display:flex;
    align-items:center;
    justify-content:center;
    border-radius:15px;
    background:rgba(0,170,255,.1);
    color:#00aaff;
    font-size:28px;
    margin-bottom:22px;
}

.card h3{
    font-size:22px;
    margin-bottom:12px;
}

.card p{
    color:#9298a1;
    line-height:1.6;
}

.about{
    background:#08090b;
}

.about-box{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:60px;
    align-items:center;
}

.about h2{
    font-size:45px;
    margin-bottom:20px;
}

.about h2 span{
    color:#00aaff;
}

.about p{
    color:#a5abb4;
    line-height:1.8;
    margin-bottom:20px;
}

.stats{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:15px;
}

.stat{
    background:#111419;
    border:1px solid #20252d;
    padding:25px 15px;
    text-align:center;
    border-radius:15px;
}

.stat strong{
    display:block;
    font-size:30px;
    color:#00aaff;
}

.stat small{
    color:#888f99;
}

.team{
    background:#0c0e12;
}

.team-grid{
    display:grid;
    grid-template-columns:repeat(2,1fr);
    gap:25px;
    max-width:800px;
    margin:auto;
}

.person{
    background:#111419;
    border:1px solid #20252d;
    border-radius:20px;
    overflow:hidden;
    text-align:center;
    transition:.3s;
}

.person:hover{
    transform:translateY(-7px);
    border-color:#00aaff;
}

.person-photo{
    height:280px;
    background:linear-gradient(135deg,#15191f,#08090b);
    display:flex;
    align-items:center;
    justify-content:center;
    color:#555c66;
}

.person-info{
    padding:25px;
}

.person-info h3{
    font-size:25px;
}

.person-info p{
    color:#00aaff;
    margin-top:8px;
}

.gallery{
    background:#08090b;
}

.gallery-grid{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:15px;
}

.gallery-item{
    height:260px;
    border-radius:16px;
    overflow:hidden;
    background:#111419;
    border:1px solid #20252d;
}

.gallery-item img{
    width:100%;
    height:100%;
    object-fit:cover;
    transition:.5s;
}

.gallery-item:hover img{
    transform:scale(1.08);
}

.contact{
    background:
        radial-gradient(circle at 50% 50%,rgba(0,170,255,.12),transparent 40%),
        #0c0e12;
}

.contact-box{
    max-width:850px;
    margin:auto;
    text-align:center;
    padding:55px 25px;
    border:1px solid #20252d;
    border-radius:25px;
    background:#111419;
}

.contact-box h2{
    font-size:45px;
    margin-bottom:15px;
}

.contact-box h2 span{
    color:#00aaff;
}

.contact-box p{
    color:#969ca5;
    margin-bottom:30px;
}

.contact-buttons{
    display:flex;
    justify-content:center;
    gap:15px;
    flex-wrap:wrap;
}

footer{
    background:#050608;
    border-top:1px solid #171a20;
    padding:30px 20px;
    text-align:center;
    color:#737983;
}

footer strong{
    color:#00aaff;
}

@keyframes rotate{
    from{transform:rotate(0deg);}
    to{transform:rotate(360deg);}
}

@media(max-width:800px){

    nav{
        display:none;
        position:absolute;
        top:80px;
        left:0;
        width:100%;
        background:#08090b;
        flex-direction:column;
        padding:25px;
        text-align:center;
    }

    nav.active{
        display:flex;
    }

    .menu{
        display:block;
    }

    .cards{
        grid-template-columns:1fr;
    }

    .about-box{
        grid-template-columns:1fr;
    }

    .team-grid{
        grid-template-columns:1fr;
    }

    .gallery-grid{
        grid-template-columns:1fr 1fr;
    }

    .gallery-item{
        height:200px;
    }

    .section-title h2,
    .about h2,
    .contact-box h2{
        font-size:34px;
    }
}

@media(max-width:500px){

    .gallery-grid{
        grid-template-columns:1fr;
    }

    .hero p{
        font-size:16px;
    }

    .btn{
        width:100%;
    }

    .stats{
        grid-template-columns:1fr;
    }
}
</style>
</head>

<body>

<header>
    <div class="nav">
        <div class="logo">TORNADO<span>.</span></div>

        <nav id="nav">
            <a href="#pocetna">Почетна</a>
            <a href="#uslugi">Услуги</a>
            <a href="#tim">Тим</a>
            <a href="#galerija">Галерија</a>
            <a href="#kontakt">Контакт</a>
        </nav>

        <div class="menu" onclick="toggleMenu()">☰</div>
    </div>
</header>

<section class="hero" id="pocetna">
    <div class="hero-content">

        <div class="badge">ПРОФЕСИОНАЛНА АВТОПЕРАЛНА</div>

        <h1>
            ТВОЈОТ АВТО.<br>
            <span>НАШ СТАНДАРД.</span>
        </h1>

        <p>
            Професионално чистење и нега на автомобили.
            Детали што се гледаат, квалитет што се чувствува.
        </p>

        <div class="buttons">
            <a href="#uslugi" class="btn btn-primary">Погледни услуги</a>
            <a href="#kontakt" class="btn btn-secondary">Контактирај нè</a>
        </div>

    </div>
</section>

<section class="services" id="uslugi">
    <div class="container">

        <div class="section-title">
            <h2>Наши <span>услуги</span></h2>
            <p>Сè што му треба на твојот автомобил.</p>
        </div>

        <div class="cards">

            <div class="card">
                <div class="icon">🚿</div>
                <h3>Комплетно перење</h3>
                <p>
                    Темелно надворешно и внатрешно чистење
                    за совршено чист автомобил.
                </p>
            </div>

            <div class="card">
                <div class="icon">✨</div>
                <h3>Деталинг</h3>
                <p>
                    Детално чистење на ентериерот и екстериерот
                    со внимание на секој детаљ.
                </p>
            </div>

            <div class="card">
                <div class="icon">💎</div>
                <h3>Полирање</h3>
                <p>
                    Освежување на изгледот и сјајот на
                    каросеријата на твојот автомобил.
                </p>
            </div>

            <div class="card">
                <div class="icon">🧽</div>
                <h3>Длабинско чистење</h3>
                <p>
                    Длабинско чистење на седишта,
                    теписи и внатрешни површини.
                </p>
            </div>

            <div class="card">
                <div class="icon">🛞</div>
                <h3>Чистење фелни</h3>
                <p>
                    Темелно чистење на фелни и отстранување
                    на нечистотии од сопирачките.
                </p>
            </div>

            <div class="card">
                <div class="icon">🔥</div>
                <h3>Професионална нега</h3>
                <p>
                    Користиме квалитетни производи за
                    долготраен чист и свеж изглед.
                </p>
            </div>

        </div>
    </div>
</section>

<section class="about">
    <div class="container">

        <div class="about-box">

            <div>
                <h2>Зошто <span>Торнадо?</span></h2>

                <p>
                    Кај нас автомобилот не е само превозно средство.
                    Секое возило го третираме со внимание и посветеност.
                </p>

                <p>
                    Нашата цел е секој клиент да си замине задоволен
                    и автомобилот повторно да изгледа како нов.
                </p>
            </div>

            <div class="stats">

                <div class="stat">
                    <strong>100%</strong>
                    <small>Посветеност</small>
                </div>

                <div class="stat">
                    <strong>24/7</strong>
                    <small>Контакт</small>
                </div>

                <div class="stat">
                    <strong>TOP</strong>
                    <small>Квалитет</small>
                </div>

            </div>

        </div>
    </div>
</section>

<section class="team" id="tim">
    <div class="container">

        <div class="section-title">
            <h2>Нашиот <span>тим</span></h2>
            <p>Луѓето зад Автоперална Торнадо.</p>
        </div>

        <div class="team-grid">

            <div class="person">
                <div class="person-photo">
                    ФОТОГРАФИЈА
                </div>

                <div class="person-info">
                    <h3>Тео</h3>
                    <p>Газда / Сопственик</p>
                </div>
            </div>

            <div class="person">
                <div class="person-photo">
                    ФОТОГРАФИЈА
                </div>

                <div class="person-info">
                    <h3>Лео</h3>
                    <p>Член на тимот</p>
                </div>
            </div>

        </div>

    </div>
</section>

<section class="gallery" id="galerija">
    <div class="container">

        <div class="section-title">
            <h2>Нашата <span>галерија</span></h2>
            <p>Погледни дел од нашата работа.</p>
        </div>

        <div class="gallery-grid">

            <div class="gallery-item">
                <img src="slika1.jpg" alt="Автомобил">
            </div>

            <div class="gallery-item">
                <img src="slika2.jpg" alt="Автомобил">
            </div>

            <div class="gallery-item">
                <img src="slika3.jpg" alt="Автомобил">
            </div>

            <div class="gallery-item">
                <img src="slika4.jpg" alt="Автомобил">
            </div>

            <div class="gallery-item">
                <img src="slika5.jpg" alt="Автомобил">
            </div>

            <div class="gallery-item">
                <img src="slika6.jpg" alt="Автомобил">
            </div>

        </div>

    </div>
</section>

<section class="contact" id="kontakt">
    <div class="container">

        <div class="contact-box">

            <h2>Контактирај <span>нè</span></h2>

            <p>
                За термин или дополнителни информации,
                контактирај нè директно.
            </p>

            <div class="contact-buttons">

                <a href="tel:+38970000000" class="btn btn-primary">
                    📞 Јави се
                </a>

                <a href="https://www.google.com/maps" target="_blank"
                   class="btn btn-secondary">
                    📍 Локација
                </a>

            </div>

        </div>

    </div>
</section>

<footer>
    © 2026 <strong>Автоперална Торнадо</strong> — Сите права се задржани.
</footer>

<script>

function toggleMenu(){
    document.getElementById("nav").classList.toggle("active");
}

document.querySelectorAll("nav a").forEach(link=>{
    link.addEventListener("click",()=>{
        document.getElementById("nav").classList.remove("active");
    });
});

</script>

</body>
</html>
```
