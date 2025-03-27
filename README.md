<!DOCTYPE html>
<html lang="en">
<head>

	<meta charset="UTF-8">
	<meta http-equiv="X-UA-Compatible" content="IE=edge">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">

	<title>Document</title>

	<link rel="stylesheet" href="css/main.css">

	<script src="libs/gsap/gsap.min.js" defer></script>
	<script src="libs/gsap/ScrollTrigger.min.js" defer></script>
	<script src="libs/gsap/ScrollSmoother.min.js" defer></script>

	<script src="js/app.js" defer></script>

</head>
<body>


	<div class="top-line">
		<div class="container container-top">
			<div>
				<!-- <div class="logo">
					<img src="img/logo.svg" alt="Alt">
				</div> -->
			</div>
			<div>
				<ul class="main-mnu">
					<li><a href="file:///C:/Users/Ярослав/Desktop/shopping-cart/index2.html">Методичка УФСИН</a></li>
					<li><a href="#">Информация о сайте</a></li>
					<li><a href="#">Видеоролик</a></li>
					<li><a href="file:///C:/Users/Ярослав/Desktop/showcase-3d-effect/ready-html/index.html">Руководящий состав</a></li>
					<li><a href="file:///C:/Users/Ярослав/Desktop/server3/ready-html/index.html">Руководство подразделений</a></li>
				</ul>
			</div>
		</div>
	</div>
	
	
	<div class="wrapper">
		<div class="content">

			<header class="main-header">
				<div class="layers">
					<div class="layer__header">
						<div class="layers__caption">Официальный сайт</div>
						<div class="layers__title">ГУФСИН по <br>Нижнегородской области</div>
					</div>
					<div class="layer layers__base" style="background-image: url(img/layer-base.png);"></div>
					<div class="layer layers__middle" style="background-image: url(img/layer-middle.png);"></div>
					<div class="layer layers__front" style="background-image: url(img/layer-front.png);"></div>
				</div>
			</header>
		
			<article class="main-article" style="background-image: url(img/dungeon.jpg);">
				<div class="main-article__content">
					<h2 class="main-article__header">ФСИН</h2>
					<p class="main-article__paragraph">Федеральная служба исполнения наказаний (ФСИН России) — федеральный орган исполнительной власти России, осуществляющий функции по контролю и надзору в сфере исполнения уголовных наказаний в отношении осуждённых, содержанию лиц, подозреваемых либо обвиняемых в совершении преступлений, и подсудимых, находящихся под стражей, их охране и конвоированию. </p>
				</div>
				<div class="copy">© Amazing RolePlay <br> Сервер: SKY</div>
			</article>

		</div>
	</div>

</body>
</html>

/* USER VARIABLES SECTION */

:root {
	--accent: #CC8869;
	--text: #333;
	--regular-text: 16px;
	--lineheight: 1.65;
	--userfont: roboto-st, sans-serif;
	--systemfont: -apple-system, BlinkMacSystemFont, Arial, sans-serif;
	--padding: 120px;
	--transition: cubic-bezier(.4, 0, 0, 1);
}

/* BOOTSTRAP SETTINGS SECTION */

/* gutter 20px (10px + 10px). Comment this code for default gutter start at 1.5rem (24px) wide. */
.container, .container-fluid, .container-lg, .container-md, .container-sm, .container-xl, .container-xxl { --bs-gutter-x: .625rem; }
.row, .row > * { --bs-gutter-x: 1.25rem; }

/* FONTS LOAD SECTION */

@font-face { src: url("../fonts/roboto-regular-webfont.woff2") format("woff2"); font-family: "roboto-st"; font-weight: 400; font-style: normal; }
@font-face { src: url("../fonts/roboto-italic-webfont.woff2") format("woff2"); font-family: "roboto-st"; font-weight: 400; font-style: italic; }
@font-face { src: url("../fonts/roboto-bold-webfont.woff2") format("woff2"); font-family: "roboto-st"; font-weight: 700; font-style: normal; }
@font-face { src: url("../fonts/roboto-bolditalic-webfont.woff2") format("woff2"); font-family: "roboto-st"; font-weight: 700; font-style: italic; }
@font-face { src: url("../fonts/assassin.woff2") format("woff2"); font-family: "assassin-st"; font-weight: 700; font-style: italic; }

/* GENERAL CSS SETTINGS */

::placeholder { color: #666; }
::selection { background-color: var(--accent); color: #fff; }
input, textarea { outline: none; }
input:focus:required:invalid, textarea:focus:required:invalid { border-color: red; }
input:required:valid, textarea:required:valid { border-color: green; }

body {
	font-family: var(--userfont);
	font-size: var(--regular-text);
	line-height: var(--lineheight);
	color: var(--text);
	min-width: 320px;
	position: relative;
	overflow-x: hidden;
}

/* USER STYLES */

body, html {
	height: 100%;
}

.showcase {
	background-color: #000;
	height: 100%;
	position: relative;
	color: #fff;
	/* overflow: hidden; */
}
.showcase::before {
	content: '';
	width: 100%;
	height: 100%;
	position: absolute;
	z-index: 1;
	box-shadow: inset 0 0 500px #000;
}
.showcase::after {
	content: '';
	position: absolute;
	top: 0;
	right: 0;
	bottom: 0;
	left: 0;
	background-image: url(../images/light.png);
	background-size: cover;
	background-repeat: no-repeat;
	background-position: center -65px;
	animation: k-light 3s ease-in-out infinite;
}
.showcase__video {
	position: absolute;
	top: 0;
	left: 0;
	width: 100%;
	height: 100%;
	object-fit: cover;
	opacity: .48;
}
.showcase__content-wrapper {
	position: relative;
	z-index: 2;
	height: 100%;
	padding: var(--padding) 0;
}
.showcase__content-wrapper::before {
	content: '';
	position: absolute;
	top: 0;
	right: 0;
	bottom: 0;
	left: 0;
	background-image: url(../images/glow.png);
	background-position: center;
	background-repeat: no-repeat;
	background-size: cover;
	animation: k-glow 1.6s ease-in-out infinite;
}
.showcase__header {
	position: absolute;
	text-align: center;
	width: 100%;
	z-index: 1;
	top: 40px;
	font-family: assassin-st, sans-serif;
	font-size: 32px;
	color: rgba(255, 255, 255, .75);
}
.showcase__header span {
	color: var(--accent);
}



.container {
	margin: auto;
	max-width: 840px;
}
.container-top {
	display: flex;
	justify-content: space-between;
}
.top-line {
	position: absolute;
	width: 90%;
	z-index: 10;
	padding: 1.7rem 0;
}
.logo {
	border: 3px solid #E1E6F7;
	border-radius: 10em;
	width: 54px;
	height: 54px;
	display: flex;
	align-items: center;
	justify-content: center;
	opacity: .75;
}
.logo img{
	width: 25px;
	height: auto;
}
.main-mnu {
	display: flex;
	margin-top: 15px;
	font-size: 20.2px;
	margin-right: -16px;
}
.main-mnu li {
	list-style: none;
}
.main-mnu a {
	color: #bbbec9;
	padding: 16px;
	font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
	text-decoration: none;
	font-weight: 200;
	outline: none;
}
.main-mnu a:hover {
	text-decoration: underline;
}



.showcase__header10 span {
	color: var(--accent);
}
.showcase-carousel .swiper-wrapper {
	transition: var(--transition);
}
.showcase-carousel__item {
	position: relative;
	height: calc(100vh - var(--padding)*2);
	text-align: center;
	opacity: .25;
	transform: scale(.75);
	transition: opacity 1.8s var(--transition), transform 1.8s var(--transition)
}
.showcase-carousel__item::after {
	content: '';
	width: 120px;
	height: 0;
	position: absolute;
	box-shadow: 0 0 45px 10px #010101;
	bottom: 5px;
	left: calc(50% - 60px);
}
.showcase-carousel__item p {
	position: absolute;
	bottom: -85px;
	width: 100%;
	font-family: assassin-st, sans-serif;
	font-size: 32px;
	color: rgba(255, 255, 255, .5);
	text-shadow: rgb(58 78 94) 0 0 10px;
}
.showcase-carousel__item.swiper-slide-active {
	opacity: .8;
	transform: scale(.98);
}
.showcase-carousel__image-wrapper > * {
	position: absolute;
	width: 100%;
	height: 100%;
	perspective: 150px;
	transform-style: preserve-3d;
}
.showcase-carousel__image {
	position: absolute;
	width: 100%;
	height: 100%;
	background-size: contain;
	background-position: center;
	background-repeat: no-repeat;
}
.showcase-carousel__image-left {
	perspective-origin: left center;
	clip-path: polygon(0 0, 50% 0, 50% 100%, 0 100%);
}
.showcase-carousel__image-right {
	perspective-origin: right center;
	clip-path: polygon(50% 0, 100% 0, 100% 100%, 50% 100%);
	/* Фикс вертикальной полосы на некоторых дисплеях */
	margin-left: -.55px
}
.showcase-carousel__image-left .showcase-carousel__image {
	animation: k-left-side 2s ease-in-out infinite;
	animation-direction: alternate;
}
.showcase-carousel__image-right .showcase-carousel__image {
	animation: k-right-side 2s ease-in-out infinite;
	animation-direction: alternate;
}

/* NAVIGATION */

.showcase-navigation {
	overflow: hidden;
	position: absolute;
	z-index: 2;
	top: 0;
	right: 0;
	bottom: 0;
	left: 0;
}
.showcase-navigation > * {
	position: absolute;
	height: 100%;
	width: 50%;
	outline: none;
	cursor: pointer;
}
.showcase-navigation__next {
	right: 0;
}
.showcase-navigation > *::before {
	content: '?';
	font-family: assassin-st;
	opacity: 0;
	transition: opacity .75s ease-out;
	position: absolute;
	transform: rotate(-90deg);
	left: 50px;
	top: 50%;
	font-size: 45px;
}
.showcase-navigation > *:hover::before {
	opacity: .25;
}
.showcase-navigation__next::before {
	transform: rotate(90deg);
	right: 50px;
	left: auto;
}
.showcase-navigation > *.swiper-button-disabled {
	display: none;
}

/* ANIMATIONS */

@keyframes k-light {
	0% {
		opacity: .2;
	}
	50% {
		opacity: .3;
	}
	100% {
		opacity: .2;
	}
}
@keyframes k-glow {
	0% {
		opacity: .6;
	}
	50% {
		opacity: .8;
	}
	100% {
		opacity: .6;
	}
}
@keyframes k-left-side {
	0% {
		transform: rotateY(-1deg) scaleX(.92);
	}
	100% {
		transform: rotateY(0deg) scaleX(1);
	}
}
@keyframes k-right-side {
	0% {
		transform: rotateY(0deg) scaleX(1);
	}
	100% {
		transform: rotateY(1deg) scaleX(.92);
	}
}
