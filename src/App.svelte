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


