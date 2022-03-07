<script>
	import { Router, Link, Route } from "svelte-routing";
	import About from "./Pages/About.svelte";
	import Portfolio from "./Pages/Portfolio.svelte";
  import Contact from "./Pages/Contact.svelte";
  import Home from "./Pages/home.svelte";
</script>
<head>
  <meta name="viewport" content="width=device-width, initial-scale=1">
</head>

<div class="main">
  <div class="header">
	  <Router>
    <nav>
      <ul>
       <li><img id="logo" src="code.png" alt="dawn" to="/"></li>
       <li class="link"><Link style={"color: white; text-decoration: none;"}  to="/">Home</Link></li>
       <li class="link"><Link style={"color: white; text-decoration: none;"}  to="about">About</Link></li>
       <li class="link"><Link style={"color: white; text-decoration: none;"}  to="portfolio">Projects</Link></li>
       <li class="link"><Link style={"color: white; text-decoration: none;"}  to="contact">Contact</Link></li>
      </ul>
    </nav>
	<Route path="/" component="{Home}"></Route>
    <Route path="about" component="{About}" />
	<Route path="portfolio" component="{Portfolio}" />
  <Route path="contact" component="{Contact}" />
</Router>

	
	  
  </div>
</div>

<style>
  html, body {
	position: relative;
	width: 100%;
	height: 100%;
}

body {
	color: #333;
	margin: 0;
	box-sizing: border-box;
	font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen-Sans, Ubuntu, Cantarell, "Helvetica Neue", sans-serif;
}

/* App */
@import url('https://fonts.googleapis.com/css2?family=Raleway:wght@500&display=swap');
.header {
  font-family: 'Raleway', sans-serif;
  color: #EEEEEE;
  
}

.app-item{
  width: 22rem;
  height: 22rem;
}

.main{
	height: 100vh;
	background-color: #222831;
}

nav{
  text-align: center;
  padding: 1em;
  margin: 0 auto;
}

ul {
  list-style-type: none;
  overflow: hidden;
  display: flex;
  flex-direction: row;
  row-gap: 150px;
color: white;
}
 .link{
	 padding-left:50px ;
	 cursor: pointer;
   text-decoration: none;
 }
 .link:hover{
   color: #00adb5;
   text-decoration:underline;
 }
 

#logo{
	width: 50px;
	height: 50px;
}


@media (max-width: 600px) {
  .link {
	padding-left: 20px;
  }

}

/* App */

/* Home */
.display-intro-home {
    display: inline-flex;
  }

  .intro-home {
    padding: 90px;
    padding-right: 10px;
    margin-top: 50px;
    flex: 1;
  }

  .name-home {
    color: #00adb5;
  }

  .space-home {
    margin-right: 120px;
    width: 100%;
    padding: 5px;
    flex: 1;
  }

  .home-img {
   max-width: 100%;
   
  }

  @media (max-width: 900px) {
   .display-intro-home {
     flex-direction: column;
     background-color: #222831;
   }

   .intro-home {
     padding: 10px;
     margin-top: 20px;
   }

   .space-home {
     padding: 0px;
   }

  }


/* Home */

/* About */
.About-me {
    font-family: "Raleway", sans-serif;
    color: #eeeeee;
    display: inline-flex;
    justify-content: space-between;
  }

  .About {
    padding: 90px;
    margin-top: 30px;
    flex: 1;
  }

  .coding {
    margin-right: 120px;
    flex: 1;
    
  }

  .about-img{
    
    max-width: 120%;
    
  }

  .fab {
    font-size: 5rem;
  }


  @media (max-width: 1000px){
    .About-me{
      flex-direction: column;
      background-color: #222831;
    }

    .About {
      padding: 10px;
     margin-top: 20px;
    }

    .about-img{
    
    max-width: 100%;
    
  }

  }
/* About */

/* Portfolio */
.Project {
    font-family: "Raleway", sans-serif;
    color: #eeeeee;
    height: fit-content;
    background-color: #222831;
  }

  .collection {
    padding: 90px;
    padding-top: 20px;
    padding-bottom: 20px;
  }

  .apps{
     display: grid;
     grid-template-columns: auto auto auto;
     gap: 20px;
     
  }

  .app-item{
     margin: 20px;
     text-align: center;
     background-color: white;
     border-radius: 7%;
     color: black;
     height: 22em;
  }

  .app-image{
      max-width: 100%;
      height: 55%;
      border-radius: 5%;
  }
  .app-image:hover {
    filter: grayscale(100%) blur(2px);
  }

  .project-name{
  font-weight: bolder;  
  }

  .project-description {
      font-weight: 100;
      color: grey;
      padding-left: 1em;
      padding-right: 1em;
  }


  @media (max-width: 1000px) {

   .apps{
    grid-template-columns: auto;
   }

   .app-item {
       margin-top: 20px;
       margin-bottom: 20px;
      
   }

   .Project {
       background-color: #222831;
       background-size: contain;
   }

   .collection {
       padding: 50px;
       padding-top: 0px;
   }
  }
/* Portfolio */

/* Contact */
.Contact-me {
    font-family: "Raleway", sans-serif;
    color: #eeeeee;
    display: inline-flex;
  }

  .Contact {
    padding: 90px;
    margin-top: 20px;
    flex: 1;
  }

  .coding {
    flex: 1;
  }

  .title {
    color: #00adb5;
    margin: 0px;
  }

  .contact-img{
      max-width: 100%;
      
  }

  .contact-btn{
      padding: 10px 20px 10px 20px;
      background-color: #00adb5;
      color: white;
      border: 1px solid #00adb5;
      border-radius: 7%;
      text-decoration: none;
  }
  .contact-btn:hover {
    background-color: #00e2ee;
  }

  .social-item {
      margin-top: 50px;
      
  }



  .social-item:hover {
      color: #00e2ee;
  }

  .social-link{
    text-decoration: none;
      color: white;
  }
  .social-link:hover {
    color: #00e2ee;
  }

  @media (max-width: 600px) {
   .Contact-me {
       flex-direction: column;
       background-color: #222831;
   }

   .Contact {
    padding: 20px;
    margin-top: 10px;
   }

   

  }
/* Contact */

.transition {
    animation-name: fadeInUp;
    animation-duration: 0.25s;
    transition-timing-function: ease-in;
    animation-fill-mode: both;
  }
  
  @keyframes fadeInUp {
  0% {
    opacity: 0;
    transform: translate3d(0, 100%, 0);
  }

  100% {
    opacity: 1;
    transform: none;
  }
}

@media (max-width: 375px) {
 ul {
   row-gap: 100px;
   margin-left: -40px;
 }

 .link{
   padding-left: 15px;
   
 }

 li{
  font-size: 0.8rem;
 }

 .app-item{
  width: 18rem;
  height: 18rem;
}

 

}
</style>
