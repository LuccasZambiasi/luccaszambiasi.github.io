<!DOCTYPE html>
<html lang="en" >
<head>
    <meta charset="UTF-8">
    <title>Oie!</title>
    <link rel='stylesheet' href='https://cdnjs.cloudflare.com/ajax/libs/bulma/0.7.4/css/bulma.min.css'>
    <script src='https://use.fontawesome.com/releases/v5.3.1/js/all.js'></script>
    <script src='https://cdnjs.cloudflare.com/ajax/libs/jquery/3.3.1/jquery.min.js'></script>
</head>
    <style>
    html,
body {
  margin: 0;
  height: 100%;
}

body,
footer,
.hero-body {
  background-color: rgb(10, 25, 47) !important;
}


a {
  color: inherit;
}

a:hover {
  text-decoration: none;
  color: inherit;
}

p {
  color: rgb(136, 146, 176);
}

.title {
  color: rgba(139, 180, 216, 0.94);
}

.sidebar {
  background-color: rgb(23, 42, 69);
  display: flex;
  align-items: center;
  flex-direction: column;
  border-radius: 5px;
  color: rgb(136, 146, 176);
  opacity: 1;
}

.sidebar-link {
  font-size: 0.8rem;
  text-transform: uppercase;
  color: rgba(139, 180, 216, 0.94);
}

.sidebar-link:hover {
  color: rgb(230, 241, 255);
}
.header-name {
  font-weight: 600;
  color: rgb(230, 241, 255);
}

.column-header {
  border-bottom: 2px rgb(45, 57, 82) solid;
  margin-bottom: 1rem;
}

.column-header > h1 {
  font-family: "Lato", sans-serif;
  font-weight: 100;
  color: white;
}

.icon,
.sidebar-link {
  transition-duration: 250ms;
}

.icon:hover {
  color: white;
}

.terminal-bar {
  background-color: #eae8e9;
  border-top-left-radius: 5px;
  border-top-right-radius: 5px;
  display: flex;
  position: relative;
}

.dark-mode {
  background-image: linear-gradient(180deg, #464248 0%, #3b383d 100%);
  border-bottom: 1px solid rgba(66, 66, 66, 0.5);
}

.dark-mode-text {
  color: #bdb9bf !important;
}

.icon-btn {
  border-radius: 50%;
  margin-top: 7px;
  height: 15px;
  width: 15px;
  margin-bottom: 0.5rem;
}

.terminal-bar > div.icon-btn:first-child {
  margin-left: 0.6rem;
}

.terminal-bar > div.icon-btn:not(:first-child) {
  margin-left: 0.5rem;
}

.terminal-bar > div.icon-btn:last-child {
  margin-right: 0.6rem;
}

.close {
  background-color: #fa615c;
}

.max {
  background-color: #3fc950;
}

.min {
  background-color: #ffbd48;
}

.terminal-window {
  background-color: black;
  border-bottom-right-radius: 5px;
  border-bottom-left-radius: 5px;
  height: 350px; /*  254px - foto sozinho: 500px */ 
  padding: 1rem;
  display: flex;
  flex-direction: column;
}

.primary-bg {
  background-color: rgb(23, 42, 69);
}

.shadow {
  -webkit-box-shadow: 0 5px 10px rgba(0, 0, 0, 0.55);
  -moz-box-shadow: 0 5px 10px rgba(0, 0, 0, 0.55);
  box-shadow: 0px 3px 15px rgba(0, 0, 0, 0.2);
}

.terminal-bar-text {
  position: absolute;
  margin-top: 3px;
  color: #383838;
  width: 100%;
  text-align: center;
  font-weight: 500;
}

.has-equal-height {
  height: 100%;
  display: flex;
  flex-direction: column;
}

.terminal-output {
  overflow-y: hidden;
  overflow: auto;
}

.column-child {
  flex: 1;
}

.terminal-line {
  position: relative;
  font-family: "Anonymous Pro", monospace;
  font-size: 0.9rem;
  color: #b7c5d2;
}

.directory {
  color: #75e1e7;
  font-weight: 500;
}

.success {
  color: #8dd39e;
}

.code,
.error,
.fa-heart {
  color: #d7566a;
}

.fa-heart {
  padding-top: 0.5rem;
}

.dummy-keyboard {
  opacity: 0;
  filter: alpha(opacity=0);
}

::-webkit-scrollbar {
  display: none;
}

@media screen and (max-width: 768px) {
  .resume {
    padding-bottom: 0.5rem;
  }
}

/* ini: Preloader */
 
#preloader {
    position:fixed;
    top:0;
    left:0;
    right:0;
    bottom:0;
    background-color: rgb(10, 25, 47); /* cor do background que vai ocupar o body */
    z-index:999; /* z-index para jogar para frente e sobrepor tudo */
}
#preloader .inner {
    position: absolute;
    top: 50%; /* centralizar a parte interna do preload (onde fica a animação)*/
    left: 50%;
    transform: translate(-50%, -50%);  
}
.bolas > div {
  display: inline-block;
  background-color: #fff;
  width: 25px;
  height: 25px;
  border-radius: 100%;
  margin: 3px;
  -webkit-animation-fill-mode: both;
  animation-fill-mode: both;
  animation-name: animarBola;
  animation-timing-function: linear;
  animation-iteration-count: infinite;
   
}
.bolas > div:nth-child(1) {
    animation-duration:0.75s ;
    animation-delay: 0;
}
.bolas > div:nth-child(2) {
    animation-duration: 0.75s ;
    animation-delay: 0.12s;
}
.bolas > div:nth-child(3) {
    animation-duration: 0.75s  ;
    animation-delay: 0.24s;
}
 
@keyframes animarBola {
  0% {
    -webkit-transform: scale(1);
    transform: scale(1);
    opacity: 1;
  }
  16% {
    -webkit-transform: scale(0.1);
    transform: scale(0.1);
    opacity: 0.7;
  }
  33% {
    -webkit-transform: scale(1);
    transform: scale(1);
    opacity: 1; 
  } 
}
/* end: Preloader */



    </style>
<body>    
    <script>
    //<![CDATA[
$(window).on('load', function () {
    $('#preloader .inner').fadeOut();
    $('#preloader').delay(350).fadeOut('slow'); 
    $('body').delay(350).css({'overflow': 'visible'});
})
//]]>
    </script>
    <div id="preloader">
        <div class="inner">
           <div class="bolas">
              <div></div>
              <div></div>
              <div></div>                    
           </div>
        </div>
    </div>
<section class="hero is-fullheight">
  <div class="hero-body">
    <div class="container">
      <div class="columns">
        <div class="column is-flex">
          <div class="column-child terminal shadow">
            <div class="terminal-bar dark-mode">
              <div class="icon-btn close"></div>
              <div class="icon-btn min"></div>
              <div class="icon-btn max"></div>
              <div class="terminal-bar-text is-hidden-mobile dark-mode-text">admin@lucaspc: ~</div>
            </div>
            <div class="terminal-window primary-bg" onclick="document.getElementById('dummyKeyboard').focus();">
              <div class="terminal-output" id="terminalOutput">
                <div class="terminal-line">
                  <center><h1><span class="help-msg"><span class="code">Oie =)</span></span></h1> <br>
                      <span class="help-msg">Tuuuudo bom? se tá lendo isso foi pq teve o trabalhão de colocar o link no google jkksksksksk</span> <br>
					  <span class="help-msg">enfim, espero q esteja gostando do livro ^~^</span> <br>
                      <br>
                  <img src="https://media0.giphy.com/media/5WgViULHvtLPRTmW5C/giphy.gif" style="height: 200px; width: 200px;"></center>
				  <span class="help-msg">- msm se algum dia alguém chegue a falar o contrário, saiba q vc é perfeita e ponto.</span> <br>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
    
  <footer class="footer">
    <div class="content has-text-centered">
      <p>
        Feito com o <i class="fas fa-heart icon"></i> no <img src="images/flag-br.png" width="20px" height="20px"/> por Lucas Zambiasi (@lucccassxd).
      </p>
    </div>
  </footer>
</section>
</body>
</html>
