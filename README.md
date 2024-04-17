<!DOCTYPE html>
<html>
<head>
    <title>NUR KAMILAAAAAA</title>
    <style>
        h1,
p {
	font-family: 'Hind', sans-serif;
}

p{
	text-indent: 50px;
}

h1 {
	font-weight: 200;
}

body {
	margin: 0px;
}

.container {
	position: relative;
	width: 100%;
	height: 100vh;
	overflow: hidden;
}

.heart {
	position: absolute;
	left: 50%;
	top: 50%;
	text-align: center;
	transform: translate(-50%, -50%);
	transition: transform 2s; /* corrected */
	z-index: 1;
}

.heart > img {
	width: 50px;
	height: auto;
}

.message {
	padding: 20px;
	background-color: #eee;
	min-width: 400px;
	height: 50%;
	position: absolute;
	left: 50%;
	top: 50%;
	transform: translate(-50%, -50%);
	z-index: 0;
	overflow: hidden;
	animation-name: openmsg;
	animation-duration: 2s;
	animation-timing-function: linear;
	animation-play-state: paused;
	animation-fill-mode: forwards;
	box-shadow: 0 10px 20px rgba(0, 0, 0, 0.19), 0 6px 6px rgba(0, 0, 0, 0.23);
	border-radius: 5px;
}

.heart > img:hover {
	animation-name: beat;
	animation-duration: 2s;
	animation-timing-function: ease-in-out;
	animation-iteration-count: infinite;
	animation-play-state: running;
}

@keyframes beat {
	0% {
		width: 50px;
	}
	25% {
		width: 58px;
	}
	30% {
		width: 50px;
	}
	50% {
		width: 45px;
	}
	60% {
		width: 50px;
	}
	75% {
		width: 58px;
	}
	100% {
		width: 50px;
	}
}

@keyframes openmsg {
	0% {
		height: 0px;
		padding: 0px 20px;
	}
	100% {
		height: 75%;
		padding: 20px 20px;
	}
}

@keyframes heartMove {
	0% {
		top: 50%;
	}
	100% {
		top: 85%;
		transform: translate(-50%, 0);
	}
}

.openNor {
	animation-direction: normal;
	animation-play-state: running;
}

.closeNor {
	animation-direction: reverse;
	animation-play-state: running;
}

.no-anim {
	animation: none;
}

.closed {
	height: 0px;
	padding: 0px 20px;
}

.bottom {
	bottom: 5px;
}

.openHer {
	animation-name: heartMove;
	animation-duration: 2s;
	animation-timing-function: linear;
	animation-play-state: running;
	animation-fill-mode: forwards;
}

.closeHer {
	animation-name: heartMove;
	animation-duration: 2s;
	animation-timing-function: linear;
	animation-play-state: running;
	animation-direction: reverse;
	animation-fill-mode: forwards;
}

.beating > img {
	animation-name: beat;
	animation-duration: 2s;
	animation-timing-function: ease-in-out;
	animation-iteration-count: infinite;
	animation-play-state: running;
}

.openedHer {
	top: 85%;
	transform: translate(-50%, 0);
}
    </style>
</head>
<body>
    <div class="container">
        <label>
            <div class="heart">
                <img src="https://raw.githubusercontent.com/DzarelDeveloper/Img/main/Lope.png">
            </div>
            <input id="messageState" type="checkbox" style="display:none">
        </label>
        <div class="message">
                <h1>Untuk Kamuu</h1> 
    <p>kamila berumur 15 tahun,dia tinggal di taman universiti,dia seorang yang baik hati malahan dia seorang yang bertanggungjawab
     <br><br>kamila merupakan seorang pengawas yang berintigriti
      <br><br>dia seoarang yang pandai,kamila fasih berkomunikasi dalam bahasa inggeris dia memasuki banyak pertandingan choral speaking.
      <br><br>Belajar elok-elok tau
   </p>
   
   <p><h1>APA YANG HASIF SUKA KAT KAMILAAAAAA</h1>
   <ol>
    <h1><li>kamila cantik</li></h1>
    <h1><li>kamila comell</li></h1>
    <h1><li>kamila kelakar</li></h1>
   </ol></p>

        </div>
    </div>

    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    <script>
        $("#messageState").on("change", (x) => {
	$(".message").removeClass("openNor").removeClass("closeNor");
	if ($("#messageState").is(":checked")) {
		$(".message").removeClass("closed").removeClass("no-anim").addClass("openNor");
		$(".heart").removeClass("closeHer").removeClass("openedHer").addClass("openHer");
		$(".container").stop().animate({"backgroundColor": "#f48fb1"}, 2000);
		console.log("I Like You");
	} else {
		$(".message").removeClass("no-anim").addClass("closeNor");
		$(".heart").removeClass("openHer").removeClass("openedHer").addClass("closeHer");
		$(".container").stop().animate({"backgroundColor": "#fce4ec"}, 2000);
		console.log("01010");
	}
});

$(".message").on('webkitAnimationEnd oanimationend msAnimationEnd animationend', function(e) {
	console.log("I Like You");
	if ($(".message").hasClass("closeNor"))
		$(".message").addClass("closed");
	$(".message").removeClass("openNor").removeClass("closeNor").addClass("no-anim");
});

$(".heart").on('webkitAnimationEnd oanimationend msAnimationEnd animationend', function(e) {
	console.log("I Like You");
	if (!$(".heart").hasClass("closeHer"))
		$(".heart").addClass("openedHer").addClass("beating");
	else
		$(".heart").addClass("no-anim").removeClass("beating");
	$(".heart").removeClass("openHer").removeClass("closeHer");
});
    </script>
</body>
</html>
