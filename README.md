# CssAnimation<html>
    <head>
 <style>
  

body{
      background-color:#81D4FA;
      overflow:hidden;
}




.fish{
 
  box-sizing: content-box;
  width: 119px;
  height: 101px;
  left:120%;
  top:0px;
  position: relative;
  border: none;
  border-radius: 50px;
  color: rgba(0,0,0,1);
  text-overflow: clip;
  background: #1abc9c;
  z-index: -1;
    transform:translateX(-400px);
    animation-name: movefromrighttoleft;
    animation-name: slide;
    animation-duration: 10s;
    animation-direction:reverse;
    animation-fill-mode: linear;
    animation-iteration-count: infinite;
  
}

.fish::before {

  box-sizing: content-box;
  position: absolute;
  content: "";
  top: 1px;
  left: 53px;
  border: 40px solid rgba(0,0,0,0);
  border-top: 0 solid;
  border-bottom: 70px solid deepskyblue;
  color: rgba(0,0,0,1);
  text-overflow: clip;
  text-shadow: none;
  transform: rotateZ(-46deg)   ;
  z-index:-2;

}

.fish::after {
  box-sizing: content-box;
  position: absolute;
  content: "";
  top: 39px;
  right: -28px;
  border: 40px solid rgba(0,0,0,0);
  border-top: 0 solid;
  border-bottom: 70px solid deepskyblue;
  color: rgba(0,0,0,1);
  text-overflow: clip;
  text-shadow: none;
  transform: rotateZ(129deg)   ;
  z-index:-2;
}

.fishtop{
box-sizing:content-box;
position:absolute;
right:72px;
top:15px;
width:20px;
height:20px;
border-radius:50%;
background-color: black;
z-index:1;
}

.fish eyeball{
    box-sizing:content-box;
position:absolute;
right:72px;
top:15px;
width:10px;
height:10px;
border-radius:50%;
background-color: white;
z-index:1;
}
.fins{
  box-sizing: content-box;
  width: 40px;
  position: absolute;
  height: 40px;
  border: none;
  border-radius: 50% / 40% 40% 60% 60%;
  color: rgba(0,0,0,1);
  text-overflow: clip;
  background: lawngreen;
  margin-top:50px;
  margin-left:50px;
  z-index:1;
}

.ball{
    box-sizing: content-box;
    width:100px;
    height:100px;
    border:none;
    border-radius:50%;
    background: salmon;
    padding:0.2%;
    position:absolute;
    
}
.ball p{
text-align: center;
    top:70%;

}
  @keyFrames movefromrighttoleft{
          from{
              transform: translateX(400px);
            

          }
          to{
             transform: translateX(-1000px); 
          }
        }
        @keyframes slide {
  0% {
    left: 0;
    top: 0;
  }

   10% {
    left: 100;
    top: 50;
  }

  50% {
    left: 244px;
    top: 100px;
  }
 70% {
    left: 44px;
    top: 10px;
  }

  80%{left: 1000px;
    top: 150;

  }

  100% {
    left: 120%;
    top: 50;
  }
}

.line{
    position:absolute;
    height: 8px;
    width:100px;
    background-color: black;
}
.left-triangle {
   width: 0;
   height: 0;
   border-right: 100px solid springgreen;
   border-top: 50px solid transparent;
   border-bottom: 50px solid transparent;
   transition:         all 100ms cubic-bezier(0.645, 0.045, 0.355, 1);
}

.skybluefish{
  width: 50px;
  height: 30px;
  margin-top: 100px;
  animation: skybluefishswim 3s infinite; 
 
}
.skybluefish1{
 
  animation: skybluefishswim 5s infinite; 
 
}
.skybluefishbody{
    background-color: #E91E63;
    position: relative;
    margin-top: 30px;
    margin-left: 40px;
    width:150px;
    height: 100px;
    border-radius: 50%;
    z-index:1;
}
.skybluefisheyeball{
  position: absolute;
  margin-left: 100px;
  margin-top: 20px;
  z-index: 1;
  background-color: white;
  border-radius: 50%;
  width: 20px;
  height: 20px;
}
.skybluefishpupil{

  position: absolute;
  z-index: 2;
  margin-left: 5px;
  margin-top: 5px;
  background-color: black;
  border-radius: 50%;
  height: 10px;
  width: 10px;
}
.skybluefishback{
  margin-top: -100px; 
  background-color: #E91E63;
  border-radius: 50%;
  transform: rotate(40deg);
  width: 80px;
  height: 50px;
  background:#9C27B0  ;
  position:relative;
}
.skybluefishbackbtm{
   margin-top: 10px; 
  background-color: #E91E63;
  border-radius: 50%;
  width: 80px;
  height: 50px;
  background:#9C27B0  ;
  position:relative;
  transform: rotate(-40deg);
}
@keyframes skybluefishswim {
  0% {
    transform: translateY(-50px) translateX(0) rotate(30deg);
  }
  25% { 
    transform: translateY(50px) translateX(250px) rotate(20deg);
  }
  50% {
    transform: translateY(100px) translateX(500px);
  }
  75% {
    transform: translateY(50px) translateX(850px) rotate(-20deg);
  }
  100% {
    transform: translateY(-170px) translateX(1200px) rotate(-40deg);
  }
}

.followmousefish{

  position:absolute;
  z-index:-1;
}

.grassbelow{
  position:absolute;
  z-index:-2;
}



body {
	background: #81D4FA;
	color: #333;
	font: 100% Lato, Arial, Sans Serif;
	height: 100vh;
	margin: 0;
	padding: 0;
	overflow-x: hidden;
}

#background-wrap {
    bottom: 0;
	left: 0;
	position: fixed;
	right: 0;
	top: 0;
	z-index: -1;
}

/* KEYFRAMES */

@-webkit-keyframes animateBubble {
    0% {
        margin-top: 1000px;
    }
    100% {
        margin-top: -100%;
    }
}

@-moz-keyframes animateBubble {
    0% {
        margin-top: 1000px;
    }
    100% {
        margin-top: -100%;
    }
}

@keyframes animateBubble {
    0% {
        margin-top: 1000px;
    }
    100% {
        margin-top: -100%;
    }
}

@-webkit-keyframes sideWays { 
    0% { 
        margin-left:0px;
    }
    100% { 
        margin-left:50px;
    }
}

@-moz-keyframes sideWays { 
    0% { 
        margin-left:0px;
    }
    100% { 
        margin-left:50px;
    }
}

@keyframes sideWays { 
    0% { 
        margin-left:0px;
    }
    100% { 
        margin-left:50px;
    }
}

/* ANIMATIONS */

.x1 {
  
	animation: animateBubble 25s linear infinite, sideWays 2s ease-in-out infinite alternate;
	
	left: -5%;
	top: 5%;
	

	transform: scale(0.6);
}

.x2 {
  
	animation: animateBubble 20s linear infinite, sideWays 4s ease-in-out infinite alternate;
	
	left: 5%;
	top: 80%;

	transform: scale(0.4);
}

.x3 {
 
	animation: animateBubble 28s linear infinite, sideWays 2s ease-in-out infinite alternate;
	
	left: 10%;
	top: 40%;
	

	transform: scale(0.7);
}

.x4 {
   
	animation: animateBubble 22s linear infinite, sideWays 3s ease-in-out infinite alternate;
	
	left: 20%;
	top: 0;

	transform: scale(0.3);
}

.x5 {
  
	animation: animateBubble 29s linear infinite, sideWays 4s ease-in-out infinite alternate;
	
	left: 30%;
	top: 50%;
	

	transform: scale(0.5);
}

.x6 {

	animation: animateBubble 21s linear infinite, sideWays 2s ease-in-out infinite alternate;
	
	left: 50%;
	top: 0;
	

	transform: scale(0.1);
}

.x7 {

	animation: animateBubble 20s linear infinite, sideWays 2s ease-in-out infinite alternate;
	
	left: 65%;
	top: 70%;
	
	-webkit-transform: scale(0.4);
	-moz-transform: scale(0.4);
	transform: scale(0.4);
}

.x8 {

	animation: animateBubble 22s linear infinite, sideWays 3s ease-in-out infinite alternate;
	
	left: 80%;
	top: 10%;
	

	transform: scale(0.3);
}

.x9 {

	animation: animateBubble 29s linear infinite, sideWays 4s ease-in-out infinite alternate;
	
	left: 90%;
	top: 50%;
	

	transform: scale(0.6);
}

.x10 {

	animation: animateBubble 26s linear infinite, sideWays 2s ease-in-out infinite alternate;
	
	left: 80%;
	top: 80%;
	
	transform: scale(0.3);
}

/* OBJECTS */

.bubble {
	border-radius: 50%;
	box-shadow: 0 20px 30px rgba(0, 0, 0, 0.2), inset 0px 10px 30px 5px rgba(255, 255, 255, 1);
	
    height: 200px;
	position: absolute;
	width: 200px;
}

.bubble:after {
    
    background: -webkit-radial-gradient(center, ellipse cover,  rgba(255,255,255,0.5) 0%,rgba(255,255,255,0) 70%); /* Chrome10+,Safari5.1+ */
    filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#80ffffff', endColorstr='#00ffffff',GradientType=1 ); /* IE6-9 fallback on horizontal gradient */

	border-radius: 50%;
	
	box-shadow: inset 0 20px 30px rgba(255, 255, 255, 0.3);
	
	content: "";
    height: 180px;
	left: 10px;
	position: absolute;
	width: 180px;
}

 </style>
 <script>
  </script>
    </head>

      <body>
<div class="followmousefish">

         <canvas id="c"></canvas>
		<script>
			var b = document.body;
			var c = document.getElementsByTagName('canvas')[0];
			var a = c.getContext('2d');
			document.body.clientWidth; 
		</script>
		<script src="main.js"></script>
    </div>
          <div class="container">
        <div class="skybluefish">
            <div class="skybluefishbody">
                <div class="skybluefisheyeball">
                    <div class="skybluefishpupil"></div>
                     </div>
              <div class="fin"></div>
                      </div> <div class="skybluefishfin"></div>
                     <div class="skybluefishback"></div>
                   
              <div class="skybluefishbackbtm"></div>
            
            </div>

             <div class="skybluefish1">
            <div class="skybluefishbody">
                <div class="skybluefisheyeball">
                    <div class="skybluefishpupil"></div>
                     </div>
              <div class="fin"></div>
                      </div> <div class="skybluefishfin"></div>
                     <div class="skybluefishback"></div>
                   
              <div class="skybluefishbackbtm"></div>
            
            </div>


           <div class="fish" style="right:-100%"><div class="fishtop"><div class="fisheyeball"></div></div><div class="fins"></div></div>
        
            </div>


<div id="background-wrap">
    <div class="bubble x1"></div>
    <div class="bubble x2"></div>
    <div class="bubble x3"></div>
    <div class="bubble x4"></div>
    <div class="bubble x5"></div>
    <div class="bubble x6"></div>
    <div class="bubble x7"></div>
    <div class="bubble x8"></div>
    <div class="bubble x9"></div>
    <div class="bubble x10"></div>
</div>
           

    </body>
</html>
