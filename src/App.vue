<script>
export default {
  name: 'App',
  data() {
    return {
      funcMenuOnOff: false,
      isActive: true
    }
  },
  methods: {
    funcMenuToggle() {
      this.funcMenuOnOff = !this.funcMenuOnOff;
    },
    localSessionBG() {
      if (document.body.style.backgroundImage === `url('./assets/320_640x21498.png')`) {
        document.body.style.setProperty('backgroundImage', 'none')
      } else {
        document.body.style.setProperty( 'backgroundImage' , `url('./assets/320_640x21498.png')`);
      }
    },
    toggler() {
      console.log('click');

      const root = document.getElementById('root');
      console.log(root.classList);

      if (!this.active) {

        this.isActive = !this.active;

        console.log(root.classList);
        // root.classList.remove('activeClass');

        this.reload();

      }
      
      if (this.active) {
        this.isActive = !this.active;
        console.log(root.classList);
      //  root.classList.add('activeClass');
       this.reload();
      }
    },
    reload() {
            this.$forceUpdate();
    },
  }
}
</script>

<!-- class="activeClass" -->

<template>
  <div id="root"
  :class="{ activeClass: isActive }"
  >
    <header>
    <img src="./assets/logo428x428.png" alt="logo" id="logo">
    <img 
    @click="funcMenuToggle"
    src="./assets/logo256x256.png" alt="logo256" id="logo256">
    <img src="./assets/logo0142857.png" alt="logo4" id="logo4">
    <h1
    @click="isActive = !isActive" :aria-pressed="isActive ? 'true' : 'false'"
    ><sup>
      <sup>
      <sup>
       <sub><sub id="V">V</sub></sub>
        <sub id="adym">a<del>dym</del>
        </sub>
        <span id="for">4</span>
        <sub><b id="C" style="text-transform: lowercase;">Č</b></sub>
        <span id="h">h</span>
        <sup id="e">e</sup>
      </sup>
    </sup>
  </sup>
    </h1>

    <label for="search">
    <input type="text" id="search">
    </label>
    <!-- <button style="padding: 0; margin: 0;"> -->

    <svg id="funcMenuToggler"
    @click="funcMenuToggle"
    style="margin-left: 0.5vw;" width="50" viewBox="0 2 24 25" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M1.5 5.28418C1.5 5.48309 1.57902 5.67386 1.71967 5.81451C1.86032 5.95516 2.05109 6.03418 2.25 6.03418H21.75C21.9489 6.03418 22.1397 5.95516 22.2803 5.81451C22.421 5.67386 22.5 5.48309 22.5 5.28418C22.5 5.08527 22.421 4.8945 22.2803 4.75385C22.1397 4.6132 21.9489 4.53418 21.75 4.53418H2.25C2.05109 4.53418 1.86032 4.6132 1.71967 4.75385C1.57902 4.8945 1.5 5.08527 1.5 5.28418ZM5.25 11.2842H21.75C21.9489 11.2842 22.1397 11.3632 22.2803 11.5038C22.421 11.6445 22.5 11.8353 22.5 12.0342C22.5 12.2331 22.421 12.4239 22.2803 12.5645C22.1397 12.7052 21.9489 12.7842 21.75 12.7842H5.25C5.05109 12.7842 4.86032 12.7052 4.71967 12.5645C4.57902 12.4239 4.5 12.2331 4.5 12.0342C4.5 11.8353 4.57902 11.6445 4.71967 11.5038C4.86032 11.3632 5.05109 11.2842 5.25 11.2842ZM12 18.0342H21.75C21.9489 18.0342 22.1397 18.1132 22.2803 18.2538C22.421 18.3945 22.5 18.5853 22.5 18.7842C22.5 18.9831 22.421 19.1739 22.2803 19.3145C22.1397 19.4552 21.9489 19.5342 21.75 19.5342H12C11.8011 19.5342 11.6103 19.4552 11.4697 19.3145C11.329 19.1739 11.25 18.9831 11.25 18.7842C11.25 18.5853 11.329 18.3945 11.4697 18.2538C11.6103 18.1132 11.8011 18.0342 12 18.0342Z" fill="#fff"/>
</svg>
<!-- </button> -->

<nav v-show="funcMenuOnOff" id="functional">
<ol>
  <li>1</li>
  <li>2</li>
  <li>3</li>
  <li>4</li>
  <li>5</li>
</ol>
</nav>

    </header>

    <div class="hero">

      <svg style="margin-bottom: 2vw;" 
      width="96" height="5" viewBox="0 0 48 2" fill="none" xmlns="http://www.w3.org/2000/svg">
<line x1="48" y1="1" x2="-8.74228e-08" y2="0.999996" stroke="#000000" stroke-width="2"/>
</svg>

      <h2 style="display: inline-block;
      margin-left: 4vw; letter-spacing: 0.2vw;">
        Hello
      </h2>

      <h2 id="I" style="font-size: 2rem; line-height: 0rem;  background: #fff; letter-spacing: -1vw; position: relative; z-index: 1;">I'm Vadym Chervoniak</h2>

      <div class="fewWords">
      <p>
        A BE / FE developer, web developer, big fan of vue.js and javascript.
      </p>
      <p>
        Of course, there's so much more to me than just a few fancy titles.
        Scroll down and get to know me,
      </p>
    </div>
    </div>

    <img class="photo" src="./assets/photo956.png" alt="photo">

    <div class="media">
      <img src="./assets/fb.png" alt="fb">
      <img src="./assets/in.png" alt="in">
      <!-- <img src="./assets/cw.png" alt="cw"> -->
<span class="ch"><b>
  Č</b></span>
      
      <img src="./assets/gh.png" alt="gh">
      <img src="./assets/tg.png" alt="tg">
    </div>

    <div class="about">
      <h2>
      Learn all about me in 60 seconds.
    </h2>

    <img src="./assets/60sec.png" alt="60sec">
    </div>

    <div class="wid">
      <h2>
        What I Do
      </h2>


      <div class="cards">




        <div class="card">
          <h3>
          FE development</h3>
          <p>
            Front-end development
          </p>
          <div class="read">Read more
          <svg width="42" height="16" viewBox="0 0 42 16" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M41.7071 8.70711C42.0976 8.31658 42.0976 7.68342 41.7071 7.29289L35.3431 0.928932C34.9526 0.538408 34.3195 0.538408 33.9289 0.928932C33.5384 1.31946 33.5384 1.95262 33.9289 2.34315L39.5858 8L33.9289 13.6569C33.5384 14.0474 33.5384 14.6805 33.9289 15.0711C34.3195 15.4616 34.9526 15.4616 35.3431 15.0711L41.7071 8.70711ZM0 9H41V7H0V9Z" fill="white"/>
</svg>

        </div>
        </div>

        <div class="card">
          <h3>
          BE development</h3>
          <p>
            Back-end development
          </p>
          <div class="read">Read more
          <svg width="42" height="16" viewBox="0 0 42 16" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M41.7071 8.70711C42.0976 8.31658 42.0976 7.68342 41.7071 7.29289L35.3431 0.928932C34.9526 0.538408 34.3195 0.538408 33.9289 0.928932C33.5384 1.31946 33.5384 1.95262 33.9289 2.34315L39.5858 8L33.9289 13.6569C33.5384 14.0474 33.5384 14.6805 33.9289 15.0711C34.3195 15.4616 34.9526 15.4616 35.3431 15.0711L41.7071 8.70711ZM0 9H41V7H0V9Z" fill="white"/>
</svg>

        </div>
        </div>

        <div class="card">
          <h3>
          Web Development</h3>
          <p>
            Full-stack web development
          </p>
          <div class="read">Read more
          <svg width="42" height="16" viewBox="0 0 42 16" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M41.7071 8.70711C42.0976 8.31658 42.0976 7.68342 41.7071 7.29289L35.3431 0.928932C34.9526 0.538408 34.3195 0.538408 33.9289 0.928932C33.5384 1.31946 33.5384 1.95262 33.9289 2.34315L39.5858 8L33.9289 13.6569C33.5384 14.0474 33.5384 14.6805 33.9289 15.0711C34.3195 15.4616 34.9526 15.4616 35.3431 15.0711L41.7071 8.70711ZM0 9H41V7H0V9Z" fill="white"/>
</svg>

        </div>
        </div>

      </div>


      <div class="caro">


        <svg width="20" height="20" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
<circle cx="10" cy="10" r="6.5" stroke="#333333" stroke-width="7"/>
</svg>

<svg width="12" height="12" viewBox="0 0 12 12" fill="none" xmlns="http://www.w3.org/2000/svg">
<circle cx="6" cy="6" r="6" fill="#333333"/>
</svg>

<svg width="12" height="12" viewBox="0 0 12 12" fill="none" xmlns="http://www.w3.org/2000/svg">
<circle cx="6" cy="6" r="6" fill="#333333"/>
</svg>



      </div>

    </div>

    <div class="folio">
      <h2>
        Portfolio
      </h2>

      <ul>
        
        <li>
          <div class="dash">&#8212;&nbsp;</div>All
        </li>
        
        <li><div class="dash">&#8212;&nbsp;</div>FE</li>
       
        <li><div class="dash">&#8212;&nbsp;</div>BE</li>
        
        <li><div class="dash">&#8212;&nbsp;</div>Web</li>

      </ul>

      <div class="tiles">


        <div class="tile">
          <img src="./assets/tile1.png" alt="tile1">
        </div>
        <div class="tile">
          <img src="./assets/tile2.png" alt="tile2">
        </div>
        <div class="tile">
          <img src="./assets/tile3.png" alt="tile3">
        </div>
        <div class="tile">
          <img src="./assets/tile4.png" alt="tile4">
        </div>
        <div class="tile">
          <img src="./assets/tile5.png" alt="tile5">
        </div>
        <div class="tile">
          <img src="./assets/tile6.png" alt="tile6">
        </div>

      </div>

      
      <div class="caro">


<svg width="20" height="20" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
<circle cx="10" cy="10" r="6.5" stroke="#333333" stroke-width="7"/>
</svg>

<svg width="12" height="12" viewBox="0 0 12 12" fill="none" xmlns="http://www.w3.org/2000/svg">
<circle cx="6" cy="6" r="6" fill="#333333"/>
</svg>

<svg width="12" height="12" viewBox="0 0 12 12" fill="none" xmlns="http://www.w3.org/2000/svg">
<circle cx="6" cy="6" r="6" fill="#333333"/>
</svg>

</div>

</div>


<div class="client">
  <h2 class="client_h2">
    Client Testimonial
  </h2>

  <img src="./assets/client1.png" alt="client">

  <svg class="client_svg" width="62" height="65" viewBox="0 0 62 65" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M21.625 32.25H12.25V24.75C12.25 20.6132 15.6132 17.25 19.75 17.25H20.6874C22.246 17.25 23.5 15.9961 23.5 14.4374V8.81256C23.5 7.254 22.2461 6 20.6874 6H19.75C9.39064 6 1 14.3906 1 24.75V52.875C1 55.9805 3.51952 58.5 6.625 58.5H21.625C24.7305 58.5 27.25 55.9805 27.25 52.875V37.875C27.25 34.7695 24.7305 32.25 21.625 32.25Z" fill="#333333"/>
<path d="M55.375 32.25H46V24.75C46 20.6132 49.3632 17.25 53.5 17.25H54.4374C55.996 17.25 57.25 15.9961 57.25 14.4374V8.81256C57.25 7.254 55.9961 6 54.4374 6H53.5C43.1406 6 34.75 14.3906 34.75 24.75V52.875C34.75 55.9805 37.2695 58.5 40.375 58.5H55.375C58.4805 58.5 61 55.9805 61 52.875V37.875C61 34.7695 58.4805 32.25 55.375 32.25Z" fill="#333333"/>
</svg>

<p>
  But I must explain to you how all this mistaken idea of denouncing pleasure and praising pain was born and I will give you a complete
</p>

<svg class="client_svg" width="60" height="53" viewBox="0 0 60 53" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M39.375 26.75H48.75V34.25C48.75 38.3868 45.3868 41.75 41.25 41.75H40.3126C38.754 41.75 37.5 43.0039 37.5 44.5626V50.1874C37.5 51.746 38.7539 53 40.3126 53H41.25C51.6094 53 60 44.6094 60 34.25V6.125C60 3.01952 57.4805 0.5 54.375 0.5H39.375C36.2695 0.5 33.75 3.01952 33.75 6.125V21.125C33.75 24.2305 36.2695 26.75 39.375 26.75Z" fill="#333333"/>
<path d="M5.625 26.75H15V34.25C15 38.3868 11.6368 41.75 7.5 41.75H6.56256C5.004 41.75 3.75 43.0039 3.75 44.5626V50.1874C3.75 51.746 5.00388 53 6.56256 53H7.5C17.8594 53 26.25 44.6094 26.25 34.25V6.125C26.25 3.01952 23.7305 0.5 20.625 0.5H5.625C2.51952 0.5 0 3.01952 0 6.125V21.125C0 24.2305 2.51952 26.75 5.625 26.75Z" fill="#333333"/>
</svg>

<h3>Jared Warner</h3>

<h4>CEO Of Zeo</h4>


 
<div class="caro">

<svg width="20" height="20" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
<circle cx="10" cy="10" r="6.5" stroke="#333333" stroke-width="7"/>
</svg>

<svg width="12" height="12" viewBox="0 0 12 12" fill="none" xmlns="http://www.w3.org/2000/svg">
<circle cx="6" cy="6" r="6" fill="#333333"/>
</svg>

<svg width="12" height="12" viewBox="0 0 12 12" fill="none" xmlns="http://www.w3.org/2000/svg">
<circle cx="6" cy="6" r="6" fill="#333333"/>
</svg>

<svg width="12" height="12" viewBox="0 0 12 12" fill="none" xmlns="http://www.w3.org/2000/svg">
<circle cx="6" cy="6" r="6" fill="#333333"/>
</svg>

</div>

</div>



<div class="contact">
  <h3>Get in touch</h3>
  <h2>Just Say Hello!</h2>
  <button>Contact</button>

  <div class="media">
    <img src="./assets/fb00.png" alt="fb">
    <img src="./assets/in00.png" alt="in">
    <!-- <img src="./assets/cw00.png" alt="cw"> -->
<span class="ch"><b>
Č</b></span>
    <span class="gh">
    <img src="./assets/github.png" alt="gh">
  </span>
    <img src="./assets/tg000.png" alt="tg">
  </div>

</div>

<div class="projects">
  <div class="project">
    <h2>750+</h2>
    <h3>Completed Projects</h3>
  </div>
  <div class="project">
    <h2>15+</h2>
    <h3>On going projects</h3>
  </div>
  <div class="project">
    <h2>250+</h2>
    <h3>Awards</h3>
  </div>
  <div class="project">
    <h2>700+</h2>
    <h3>Happy Clients</h3>
  </div>
</div>


  </div>
</template>

<style>

.activeClass {
  margin: 0;
  padding: 0;
  width: 100%;
  height: 21498px;
  background: #fff;
  background-image: url('./assets/320_640x21498.png');
  background-position: center;
  background-size: contain;
  background-repeat: no-repeat;
}



.project h2 {
  font-size: 2.5rem;
}

.projects .project {
  height: 37.5vw;
  line-height: 1rem;
  letter-spacing: -0.15vw;
}

.projects {
  margin-top: 19.1vw;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
}

.contact .media > * {
  margin: 0 6vw;
}

.contact .media
{
  margin-top: 7vw;
  height: 50.5vw;
  padding-bottom: 7.5vw;
}

.contact .media span {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.contact .media img,
.contact .media span {
  width: 7.5vw;
  height: 7.5vw;
  text-align: center;
  line-height: 7.5vw;
  border-radius: 1vw;
}

.contact .media .gh {
  margin-left: 7vw;
}

.contact .media .gh img {
  position: absolute;
  width: 6.3vw;
  height: 6.3vw;
  top: 0;
  left: 0;
  margin: 0.6vw;
}

.contact .ch, .contact .gh
{
  display: inline-block;
  background-color: white;
}

.contact .ch
{
  color: black;
  margin-top: -0.05vw;
}

.contact button
{
  height: 22.9vw;
  width: 57.9vw;
  margin-left: 21.1vw;
  margin-top: 20.2vw;
  font-size: 1.75rem;
  letter-spacing: 0.5vw;
}

.contact h2
{
  margin-left: 7.5vw;
  margin-top: 17vw;
  font-size: 2.5rem;
  letter-spacing: -0.2vw;
}


.contact h3 {
  padding-top: 29.2vw;
  font-size: 1.9rem;
  text-align: center;
  letter-spacing: 0.5vw;
  font-weight: 400;
}

.contact {
  margin-top: 16vw;
  color: #c44444;
  color: #fff;
  font-weight: 400;
  background: rgba(54, 52, 52, 1);
}

.client .caro
{
margin-top: -3vw;
margin-left: 1vw;
}

.client h4
{
margin-left: 5vw;
font-size: 1.25rem;
letter-spacing: -0.3vw;
}

.client h3 {
  margin-top: 22vw;
  margin-left: 5vw;
  font-size: 1.75rem;
  letter-spacing: 0.1vw;
}


.client p {
  margin-top: 7vw;
  line-height: 1.29rem;
  letter-spacing: 0.025vw;
  font-size: 1.15rem;
  width: 90vw;
  margin-left: 5.5vw;
}

.client_svg {
  transform: scale(2);
}

.client_svg:first-of-type {
  margin-left: 12vw;
  margin-top: 25vw;
}

.client_svg:nth-of-type(2) {
  margin-left: 80vw;
}

.client img {
  margin-top: 20vw;
  margin-left: 5vw;
  box-shadow: 0 0 0.5rem 0.25rem #44c444;
}

.client h2.client_h2 {
  text-align: left;
  font-size: 2.5rem;
  line-height: 3rem;
  margin-top: 40.5vw;
  margin-left: 5vw;
  letter-spacing: -0.001vw;
}

.folio .caro {
  margin-top:-1.5vw;
}

.tile {
  padding-bottom: 10vw;
}

.tile img {
  box-shadow: 0 0 0.5rem 0.25rem #44c444;
}

.folio .tiles {
  margin-left: 6vw;
  margin-top: 20vw;
  width: 88vw;
  height: auto;
  display: flex;
  flex-direction: column;
}

.folio ul {
  margin-top: 24.7vw;
}

.folio li {
  margin-top: 9.1vw;
  display: flex;
}

.folio h2 {
  margin-top: 46.3vw;
  text-align: center;
  font-size: 2.5rem;
  letter-spacing: 0.3vw;
}

.caro {
  display: flex;
  justify-content: center;
  align-items: center;
}

.caro svg {
  margin: 10.5vw 6.1vw;
  transform: scale(2);
}

.read {
  font-size: 1.1rem;
  font-weight: 600;
  margin: 33.9vw 0 0 6.6vw;
}

.read svg {
  transform: scale(2);
  margin-left: 9.6vw;
  
}

.card p {
  line-height: 1rem;
  margin: -5vw 0 0 6.6vw;
}

.card h3 {
  margin-left: 6.6vw;
  margin-top: 20vw;
  line-height: 3.5rem;
  font-size: 2.5rem;
}

.card {
  background: #333333;
  width: 90vw;
  height: 127.7vw;
  margin-bottom: 10vw;
  box-shadow: 0 0 0.5rem 0.25rem #44c444;
}

.card:nth-child(2),
.card:nth-child(3) {
  background: #D6D6D6;
  color: #333333;
}

.cards {
  margin-top: 23.8vw;
  margin-left: 5vw;
  width: 90vw;
  color: white;
  display: flex;
  flex-direction: column;
 
}

.wid h2 {
  margin-top: 55.4vw;
  text-align: center;
  font-size: 2.5rem;
}

.about img {
  margin-left: 5vw;
  margin-top: 10.2vw;
  box-shadow: 0 0 0.5rem 0.25rem #44c444;
}

.about h2{
  margin-top: 37.8vw;
  font-size: 2rem;
  letter-spacing: -0.15vw;
  line-height: 12vw;
  margin-left: 5vw;
}

.ch {
  margin-top: 0.2rem;
  font-size: 1.3rem;
  line-height: 1.3rem;
  /* border: 1px solid black;
  border-radius: 1vw; */
}

.media {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 43vw;
}

.media img {
  margin: 0 7vw;
  height: 6vw;

}

.media img:nth-child(2) {
  height: 7.5vw;
}

.fewWords {
  margin-top: 12vw;
}

.fewWords p {
  letter-spacing: 0.2vw;
  font-size: 1.08rem;
  line-height: 1.36rem;
}

.hero {
  padding: 7vw 5vw ;
}

img.photo {
  width: 90vw;
  height: 90vw;
  margin-left: 5vw;
  margin-top: 3vw;
  box-shadow: 0 0 0.5rem 0.25rem #44c444;
}

#V,
#adym,
#C,
#E,
#for,
#h
{
  display: inline-block;
  margin: 0;
}

#V
{
  margin: 0;
  margin-left: 1vw;
  font-size: 3rem;
}

#adym
{
  margin-left: -2.8vw;
  text-transform: capitalize;
}

#for 
{
  background-color: #44c444;
  position: relative;
  z-index: 1;
}

#C {
  position: relative;
  z-index: 1;
  margin: 0;
  margin-left: -1.7vw;
  font-size: 2.5rem;
}

#h {
  position: relative;
  text-transform: capitalize;
}

#h::after {
  content: '#';
  left: 0.4vw;
  position: absolute;
}

#e {
  margin-left: 0.142857vw;
}

#logo4
{
  visibility: hidden;
  display: block;
  position: absolute;
  height: 100%;
  z-index: -1;
}


#for::after
{
  content: '';
  position: absolute;
  background-color: #44c444;
  height: 1000px;
  z-index: -1;
  width: 2.7vw;
  top: 0;
  left: 0;
  border: inset;
  border: none;
  box-shadow: 0 0 1.42857rem 0.142857rem rgba(68, 196, 68, 1);
}

header {
  display: flex;
  position: sticky;
  width: 100%;
  top:0;
  left: 0;
  right: 0;
  z-index: 2;
}

header #logo {
  visibility: hidden;
  position: absolute;
  z-index: -2;
  max-height: 100%;
}
header #logo256 {
  position: absolute;
  z-index: -2;
  max-height: 100%;
  right: 0;
  opacity: 0.57;
}

header svg {
  position: absolute;
  right: 5vw;
  top: 12.5vw;
  box-shadow: 0 0 2.5rem 0.428571rem #333333;
  border-top-right-radius: 25%;
  border-bottom-left-radius: 100%;
}

header h1 {
  background: #fff;
  padding-left: 5vw;
  line-height: 33.3vw;
  margin: 0;
  letter-spacing: -0.442857vw;
  margin-top: -1.9vw;
}


@media screen and (max-width: 768px) {
  :root {
    font-size: 5vw;
    --mobile-height: 21498px;
  }
  header {
    width: 100%;
    height: 33.3vw;
    border: 1px solid #44c444;

}

#for::after {
  height: var(--mobile-height);
}

#search {
  visibility: hidden;
}
}



#app {
  width: 100%;
  height: auto;
}
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}

#I
{
  position: relative;
  background-color: #fff;
  height: 100%;
}
</style>
