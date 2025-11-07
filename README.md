<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title data-i18n="title">SALIH Al SALIH - Lawyer</title>
<link rel="stylesheet" href="css/style.css">
</head>
<body>

<nav>
    <ul class="navbar">
        <li><a href="index.html" data-i18n="navHome">Home</a></li>
        <li><a href="about.html" data-i18n="navAbout">About</a></li>
        <li><a href="services.html" data-i18n="navServices">Services</a></li>
        <li><a href="contact.html" data-i18n="navContact">Contact</a></li>
    </ul>
    <div id="language-switcher">
        <button onclick="setLanguage('en')">EN</button>
        <button onclick="setLanguage('ar')">AR</button>
        <button onclick="setLanguage('tr')">TR</button>
    </div>
</nav>

<header>
    <h1 data-i18n="welcome">Welcome to the Office of SALIH Al SALIH</h1>
    <p data-i18n="intro">Professional legal services tailored to your needs.</p>
</header>

<section id="services-preview">
    <h2 data-i18n="servicesTitle">Our Legal Services</h2>
    <ul>
        <li data-i18n="service1">Corporate Law</li>
        <li data-i18n="service2">Family Law</li>
        <li data-i18n="service3">Criminal Law</li>
        <li data-i18n="service4">Real Estate Law</li>
        <li data-i18n="service5">Contract Drafting</li>
    </ul>
</section>

<script src="js/i18n.js"></script>
<script>
window.onload = loadLanguage;
</script>
</body>
</html>
body { font-family: Arial, sans-serif; margin:0; padding:0; background:#f4f4f4; }
nav { background:#2c3e50; color:#fff; display:flex; justify-content:space-between; align-items:center; padding:10px 20px; }
.navbar { list-style:none; display:flex; margin:0; padding:0; }
.navbar li { margin-right:20px; }
.navbar li a { color:#fff; text-decoration:none; font-weight:bold; }
#language-switcher button { margin-left:5px; padding:5px 10px; cursor:pointer; }
header { text-align:center; padding:60px 20px; background:#34495e; color:#fff; }
header h1 { font-size:36px; margin-bottom:10px; }
section { padding:40px 20px; background:#fff; margin:20px auto; max-width:1000px; border-radius:8px; }
section h2 { color:#2c3e50; margin-bottom:20px; }
#services-preview ul { list-style:none; padding:0; }
#services-preview li { background:#ecf0f1; margin:10px 0; padding:15px; border-radius:5px; }
@media(max-width:768px){ header h1{ font-size:28px; } nav{ flex-direction:column; } .navbar li{ margin:10px 0; } }
let currentLang = 'en';

function setLanguage(lang) {
    currentLang = lang;
    loadLanguage();
}

function loadLanguage() {
    fetch(locales/${currentLang}.json)
        .then(res => res.json())
        .then(data => {
            document.querySelectorAll('[data-i18n]').forEach(el => {
                const key = el.getAttribute('data-i18n');
                if(data[key]) el.textContent = data[key];
            });
        });
}
{
    "title": "SALIH Al SALIH - Lawyer",
    "navHome": "Home",
    "navAbout": "About",
    "navServices": "Services",
    "navContact": "Contact",
    "welcome": "Welcome to the Office of SALIH Al SALIH",
    "intro": "Professional legal services tailored to your needs.",
    "servicesTitle": "Our Legal Services",
    "service1": "Corporate Law",
    "service2": "Family Law",
    "service3": "Criminal Law",
    "service4": "Real Estate Law",
    "service5": "Contract Drafting"
}
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title data-i18n="aboutTitle">About SALIH Al SALIH</title>
<link rel="stylesheet" href="css/style.css">
</head>
<body>

<nav>
    <ul class="navbar">
        <li><a href="index.html" data-i18n="navHome">Home</a></li>
        <li><a href="about.html" data-i18n="navAbout">About</a></li>
        <li><a href="services.html" data-i18n="navServices">Services</a></li>
        <li><a href="contact.html" data-i18n="navContact">Contact</a></li>
    </ul>
    <div id="language-switcher">
        <button onclick="setLanguage('en')">EN</button>
        <button onclick="setLanguage('ar')">AR</button>
        <button onclick="setLanguage('tr')">TR</button>
    </div>
</nav>

<section id="about">
    <h2 data-i18n="aboutTitle">About SALIH Al SALIH</h2>
    <p data-i18n="aboutText">SALIH Al SALIH is an experienced lawyer specializing in corporate and criminal law, providing professional legal advice and representation to clients with integrity and dedication.</p>
</section>

<script src="js/i18n.js"></script>
<script>
window.onload = loadLanguage;
</script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title data-i18n="servicesTitle">Our Legal Services</title>
<link rel="stylesheet" href="css/style.css">
</head>
<body>

<nav>
    <ul class="navbar">
        <li><a href="index.html" data-i18n="navHome">Home</a></li>
        <li><a href="about.html" data-i18n="navAbout">About</a></li>
        <li><a href="services.html" data-i18n="navServices">Services</a></li>
        <li><a href="contact.html" data-i18n="navContact">Contact</a></li>
    </ul>
    <div id="language-switcher">
        <button onclick="setLanguage('en')">EN</button>
        <button onclick="setLanguage('ar')">AR</button>
        <button onclick="setLanguage('tr')">TR</button>
    </div>
</nav>

<section id="services">
    <h2 data-i18n="servicesTitle">Our Legal Services</h2>
    <ul>
        <li data-i18n="service1">Corporate Law</li>
        <li data-i18n="service2">Family Law</li>
        <li data-i18n="service3">Criminal Law</li>
        <li data-i18n="service4">Real Estate Law</li>
        <li data-i18n="service5">Contract Drafting</li>
    </ul>
</section>

<script src="js/i18n.js"></script>
<script>
window.onload = loadLanguage;
</script>
</body>
</html>
{
    "title": "صالح الصالح - محامي",
    "navHome": "الرئيسية",
    "navAbout": "عن المحامي",
    "navServices": "الخدمات",
    "navContact": "تواصل معنا",
    "welcome": "مرحبًا بكم في مكتب صالح الصالح",
    "intro": "خدمات قانونية احترافية مصممة لتلبية احتياجاتكم.",
    "servicesTitle": "خدماتنا القانونية",
    "service1": "القانون التجاري",
    "service2": "قانون الأسرة",
    "service3": "القانون الجنائي",
    "service4": "قانون العقارات",
    "service5": "صياغة العقود",
    "aboutTitle": "عن صالح الصالح",
    "aboutText": "صالح الصالح محامي ذو خبرة في القانون التجاري والجنائي، يقدم المشورة القانونية والتمثيل المهني للعملاء بأمانة وتفانٍ.",
    "contactTitle": "تواصل معنا",
    "contactPhone": "الهاتف: +123456789",
    "contactEmail": "البريد الإلكتروني: salih@lawoffice.com",
    "contactAddress": "العنوان: شارع القانون 123، المدينة"
}
{
    "title": "SALIH Al SALIH - Avukat",
    "navHome": "Ana Sayfa",
    "navAbout": "Hakkında",
    "navServices": "Hizmetler",
    "navContact": "İletişim",
    "welcome": "SALIH Al SALIH Ofisine Hoşgeldiniz",
    "intro": "İhtiyaçlarınıza özel profesyonel hukuki hizmetler.",
    "servicesTitle": "Hukuki Hizmetlerimiz",
    "service1": "Şirket Hukuku",
    "service2": "Aile Hukuku",
    "service3": "Ceza Hukuku",
    "service4": "Gayrimenkul Hukuku",
    "service5": "Sözleşme Hazırlama",
    "aboutTitle": "SALIH Al SALIH Hakkında",
    "aboutText": "SALIH Al SALIH, şirket ve ceza hukuku alanında deneyimli bir avukattır ve müşterilere dürüstlük ve özveriyle profesyonel hukuki danışmanlık ve temsil sağlar.",
    "contactTitle": "İletişim",
    "contactPhone": "Telefon: +123456789",
    "contactEmail": "E-posta: salih@lawoffice.com",
    "contactAddress": "Adres: 123 Hukuk Sok., Şehir"
}
