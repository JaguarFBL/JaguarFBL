
<!DOCTYPE html>
<html lang="en">
	<head>
		<title> Portrait of Leonardo </title>
		<meta charset="UTF-8">
		<meta name="viewport" content="width=device-width, initial-scale=1">
		<link rel="stylesheet" href="style.css">
	</head>
 <style>
   * {
  box-sizing: border-box;
}

* {
  border: 0;
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
html {
  min-height: 100%;
}


@keyframes roll {
  0% {
    font-size:0px;
    opacity:0;
    margin-left:-30px;
    margin-top:0px;
    transform: rotate(-25deg);
  }
  3% {
    opacity:1;
    transform: rotate(0deg);
  }
  5% {
    font-size:inherit;
    opacity:1;
    margin-left:0px;
    margin-top:0px;
  }
  20% {
    font-size:inherit;
    opacity:1;
    margin-left:0px;
    margin-top:0px;
    transform: rotate(0deg);
  }
  27% {
    font-size:0px;
    opacity:0.5;
    margin-left:20px;
    margin-top:100px;
  }
  100% {
    font-size:0px;
    opacity:0;
    margin-left:-30px;
    margin-top:0px;
    transform: rotate(15deg);
  }
}

@keyframes roll2 {
  0% {
    font-size:0px;
    opacity:0;
    margin-left:-30px;
    margin-top:0px;
    transform: rotate(-25deg);
  }
  3% {
    opacity:1;
    transform: rotate(0deg);
  }
  5% {
    font-size:inherit;
    opacity:1;
    margin-left:0px;
    margin-top:0px;
  }
  30% {
    font-size:inherit;
    opacity:1;
    margin-left:0px;
    margin-top:0px;
    transform: rotate(0deg);
  }
  37% {
    font-size:1500px;
    opacity:0;
    margin-left:-1000px;
    margin-top:-800px;
  }
  100% {
    font-size:0px;
    opacity:0;
    margin-left:-30px;
    margin-top:0px;
    transform: rotate(15deg);
  }
}

@keyframes bg {
  0% {background: #ff0075;}
  3% {background: #0094ff;}
  20% {background: #0094ff;}
  23% {background: #b200ff;}
  40% {background: #b200ff;}
  43% {background: #8BC34A;}
  60% {background: #8BC34A;}
  63% {background: #F44336;}
  80% {background: #F44336;}
  83% {background: #F44336;}
  100% {background: #F44336;}
}

    @font-face {
    font-family: 'TheFont';
    
    /* Variable fonts like the one linked below allow for fine-tuned control over various font properties dynamically via CSS, such as weight ('wght'), width ('wdth'), etc. This link is where your web browser will download the font from. */
    /* Insert the link to your custom variable font */
    src: url("https://garet.typeforward.com/assets/fonts/shared/TFMixVF.woff2")
      format('woff2'); }


  body.breathe-animation {
    display: flex;
    align-items: center;
    justify-content: center;
    /* Change the Background color of the entire screen */
    background-color: black;
    /* 'vw' is a viewport-width unit, 'vh' is a viewport-height unit. 1vw equals 1% of the width of the viewport, and 1vh equals 1% of the height of the viewport. This allows the font size to scale dynamically with the window size. */
    height: 50vh;
  }

  .breathe-animation span {
    font-family: 'TheFont';
  
    /* The 'clamp()' function sets a flexible font size that will never go below a minimum value and never above a maximum value. The middle value is preferred, but it will shrink or grow based on the viewport dimensions. */
    /* Adjusts font size based on content width and viewport height */
    font-size: clamp(10vw, 20vw, 50vh);
  
    /* Change this to set the text color */
    color: white;
  
    /* Center text horizontally */
    text-align: center; 
  
    /* The 'animation' property applies the 'letter-breathe' keyframes to the element, making it animate over 3 seconds.'ease-in-out' makes the movement start and end slowly, and 'infinite' makes it repeat forever. */
    /* Controls the animation (3s is the duration) */
    animation: letter-breathe 3s ease-in-out infinite;
}
  
  /* Keyframes define the sequence of styles that an element will go through during an animation. */
  @keyframes letter-breathe {
   
    /* The 'from' and 'to' keyframes establish the initial and final states of the animation, respectively, using 'font-variation-settings'. This CSS property is used with variable fonts to adjust their weight ('wght'), width ('wdth'), etc., during the animation. */
    from,
    to {
      /* Starting weight; adjust the numbers according to your specific font */
      font-variation-settings: 'wght' 100;
    }

    /* At the midpoint (50%) of the animation, the font weight changes to 900. */
    50% {
      /* Ending weight; adjust the numbers according to your specific font */
      font-variation-settings: 'wght' 700;
    }
  }

/* Style the body */
body {
  font-family: Arial, Helvetica, sans-serif;
  margin: 0;
}

h9::before {  
  transform: scaleX(0);
  transform-origin: bottom right;
}

h9:hover::before {
  transform: scaleX(1);
  transform-origin: bottom left;
}

h9::before {
  content: " ";
  display: block;
  position: absolute;
  top: 0; right: 0; bottom: 0; left: 0;
  inset: 0 0 0 0;
  background: hsl(200 100% 80%);
  z-index: -1;
  transition: transform .3s ease;
}

h9 {
  position: relative;
  font-size: 5rem;
}



.fond1 {
color:black;
background-color:white;
background-image: Francesco_Melzi_-_Portrait_of_Leonardo.png;
margin:0;
}

/* Header/logo Title */
.header {
  padding: 1px;
  text-align: center;
  background: #ff5733;
  color: white;
}

/* Increase the font size of the heading */
.header h1 {
  font-size: 40px;
}

/* Sticky navbar - toggles between relative and fixed, depending on the scroll position. It is positioned relative until a given offset position is met in the viewport - then it "sticks" in place (like position:fixed). The sticky value is not supported in IE or Edge 15 and earlier versions. However, for these versions the navbar will inherit default position */
.navbar {
  overflow: hidden;
  background-color: #333;
  position: sticky;
  position: -webkit-sticky;
  top: 0;
}

/* Style the navigation bar links */
.navbar a {
  float: left;
  display: block;
  color: white;
  text-align: center;
  padding: 14px 20px;
  text-decoration: none;
}


/* Right-aligned link */
.navbar a.right {
  float: right;
}

/* Change color on hover */
.navbar a:hover {
  background-color: #ddd;
  color: black;
}

/* Active/current link */
.navbar a.active {
  background-color: #666;
  color: white;
}

/* Column container */
.row {  
  display: -ms-flexbox; /* IE10 */
  display: flex;
  -ms-flex-wrap: wrap; /* IE10 */
  flex-wrap: wrap;
}

/* Create two unequal columns that sits next to each other */
/* Sidebar/left column */
.side {
  -ms-flex: 30%; /* IE10 */
  flex: 30%;
  background-color: #f1f1f1;
  padding: 20px;
}

/* Main column */
.main {   
  -ms-flex: 70%; /* IE10 */
  flex: 70%;
  background-color: white;
  padding: 20px;
}

/* Fake image, just for this example */
.img {
  background-color: #aaa;
  width: 100%;
  padding: 20px;
}

/* Footer */
.footer {
  padding: 20px;
  text-align: center;
  background: #ddd;
}

/* Responsive layout - when the screen is less than 700px wide, make the two columns stack on top of each other instead of next to each other */
@media screen and (max-width: 700px) {
  .row {   
    flex-direction: column;
  }
}

/* Responsive layout - when the screen is less than 400px wide, make the navigation links stack on top of each other instead of next to each other */
@media screen and (max-width: 400px) {
  .navbar a {
    float: none;
    width: 100%;
  }
}
 </style>

	<body>
	 <div class="header">
	    <h9>Léonard de</h9>
	     <div class="breathe-animation">
             <span>Vinci</span>
         </div>
	    <h3>Un <b>Génie</b> comme personne</h3>
		<img src=Francesco_Melzi_-_Portrait_of_Leonardo.png height="150px" />
	</div>
	
	<div class="navbar">
	  <a href="#" class="active">Home</a>
	  <a href="#">Link</a>
	  <a href="#">Link</a>
	  <a href="#" class="right">Link</a>
	</div>

	<div class="row">
	  <div class="side">
		<h2>Présentation rapide</h2>
		<img src=devinci-1440x1440.jpg height="150px" />
		<p>Léonard de Vinci (italien : Leonardo di ser Piero da VinciÉcouter, dit Leonardo da Vinci), né le 14 avril 1452 du calendrier actuel à Vinci (Toscane) et mort le 2 mai 1519 à Amboise (Touraine), est un peintre polymathe toscan, simultanément artiste, organisateur de spectacles et de fêtes, scientifique, ingénieur, inventeur, anatomiste, sculpteur, peintre, architecte, urbaniste, botaniste, musicien, philosophe et écrivain.</p>
		<h3>Nationnalitée</h3>
		<p>LE PAYS DE LA PIZZA!!!!</p>
		<div> </div><br>
		<img src=th.jpg height="110px" />
		
		<br>
		<div class="fakeimg" style="height:60px;"></div>
	  </div>
	  <div class="main">
		<h2>Plus qu'un Homme, un Génie</h2>
		<h5></h5>
		<p>Vous le connaissez sûrement un génie incroyable, visionnaire et artiste. 
		<div class="fakeimg" style="height:200px;">Image</div>
		<p>Some text..</p>
		<p>Sunt in culpa qui officia deserunt mollit anim id est laborum consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco.</p>
		<br>
		<h2>TITLE HEADING</h2>
		<h5>Title description, Sep 2, 2017</h5>
		<div class="fakeimg" style="height:200px;">Image</div>
		<p>Some text..</p>
		<p>Sunt in culpa qui officia deserunt mollit anim id est laborum consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco.</p>
	  </div>
	</div>

	<div class="footer">
	  <h2>Footer</h2>
	</div>

	</body>
</html>
