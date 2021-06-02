<script>
  import { Router, Route } from "svelte-routing";
  import NavLink from "./NavLink.svelte";
  import Home from "../routes/Home.svelte";
  import Carports from "../routes/Carports.svelte";
  import AllBuildings from "../routes/AllBuildings.svelte";
  import PatioCovers from "../routes/PatioCovers.svelte";
  import RVCovers from "../routes/RVCovers.svelte";
  import Barns from "../routes/Barns.svelte";
  import LeanTos from "../routes/LeanTos.svelte";
  import HorseSheds from "../routes/HorseSheds.svelte";
  import RedIron from "../routes/RedIron.svelte";
  import WorkShops from "../routes/WorkShops.svelte";
  import GetQuote from '../routes/GetQuote.svelte';

  let navIsOpen = false;
  let top = 0;

  const handleNav = () => {
    navIsOpen = !navIsOpen;
    if (!navIsOpen) {
      window.scrollTo(0, 0);
    }
  };

  

  export let url = "";
</script>

<svelte:head>
  <link rel="preconnect" href="https://fonts.gstatic.com" />
  <link
    href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;600;900&display=swap"
    rel="stylesheet"
  />
</svelte:head>
<Router {url}>
  <nav >
    <NavLink to="/">
      <div class="logo">
        <img
          src="https://bigtexdemo.netlify.app/assets/logo.png"
          alt="Big Tex Metal Buildings Logo"
        />
      </div>
    </NavLink>
    <div class="menu">
      <NavLink to="/">Home</NavLink>

      <NavLink to="/carports">Carports</NavLink>

      <NavLink to="/patio-covers">Patio Covers</NavLink>

      <NavLink to="/rv-covers">RV Covers</NavLink>

      <NavLink to="/barns">Barns</NavLink>

      <NavLink to="/lean-tos">Lean Tos</NavLink>

      <NavLink to="/horse-sheds">Horse Sheds</NavLink>

      <NavLink to="/red-iron-metal-buildings">Red Iron</NavLink>

      <NavLink to="/workshops">Workshops</NavLink>

      <NavLink to="/get-quote">Quote</NavLink>
    </div>

    <div class="opener" on:click={handleNav} class:change={navIsOpen}>
      <div class="bar1" />
      <div class="bar2" />
      <div class="bar3" />
    </div>
  </nav>
  <div id="mySidenav" class="sidenav" class:opened={navIsOpen}>
    <div on:click={handleNav}>
      <NavLink to="/">Home</NavLink>
    </div>
    <div on:click={handleNav}>
      <NavLink to="/carports">Carports</NavLink>
    </div>
    <div on:click={handleNav}>
      <NavLink to="/patio-covers">Patio Covers</NavLink>
    </div>
    <div on:click={handleNav}>
      <NavLink to="/rv-covers">RV Covers</NavLink>
    </div>
    <div on:click={handleNav}>
      <NavLink to="/barns">Barns</NavLink>
    </div>
    <div on:click={handleNav}>
      <NavLink to="/lean-tos">Lean Tos</NavLink>
    </div>
    <div on:click={handleNav}>
      <NavLink to="/horse-sheds">Horse Sheds</NavLink>
    </div>
    <div on:click={handleNav}>
      <NavLink to="/red-iron-metal-buildings">Red Iron</NavLink>
    </div>
    <div on:click={handleNav}>
      <NavLink to="/workshops">Workshops</NavLink>
    </div>
    <div on:click={handleNav}>
      <NavLink to="/get-quote">Quote</NavLink>
    </div>
  </div>
  <div>
    <Route path="/" component={Home} />
    <Route path="all-buildings" component={AllBuildings} />
    <Route path="carports" component={Carports} />
    <Route path="patio-covers" component={PatioCovers} />
    <Route path="rv-covers" component={RVCovers} />
    <Route path="barns" component={Barns} />
    <Route path="lean-tos" component={LeanTos} />
    <Route path="horse-sheds" component={HorseSheds} />
    <Route path="red-iron-metal-buildings" component={RedIron} />
    <Route path="workshops" component={WorkShops} />
    <Route path="get-quote" component={GetQuote} />
  </div>
</Router>
<div class="content"  />

<style>
  
  /* Page content */
  .content {
    padding-top: 16px;
  }
  
  nav {
    background: #152749;
    margin: 0;
    width: 100%;
    height: 100px;
    border-bottom: 2px solid #1d3565;
    z-index: 2000;
    font-family: "Montserrat", sans-serif;
  }

  .menu {
    width: 70%;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 100%;
  }
  .menu :global(a) {
    color: white;
    text-decoration: none;
    font-size: 1.2rem;
    transition: 0.5s;
  }
  .menu :global(a:hover) {
    text-decoration: underline;
   
  }
  .logo {
    position: absolute;
    top: 10px;
    left: 20px;
  }

  .logo img {
    width: 80px;
  }
  .bar1,
  .bar2,
  .bar3 {
    width: 35px;
    height: 5px;
    background-color: white;
    margin: 6px 0;
    transition: 0.4s;
  }
  .change .bar1 {
    -webkit-transform: rotate(-45deg) translate(-9px, 6px);
    transform: rotate(-45deg) translate(-9px, 6px);
  }

  .change .bar2 {
    opacity: 0;
  }

  .change .bar3 {
    -webkit-transform: rotate(45deg) translate(-8px, -8px);
    transform: rotate(45deg) translate(-8px, -8px);
  }

  .opener {
    position: absolute;
    right: 20px;
    top: 20px;
    display: inline-block;
    cursor: pointer;
  }
  /* The side navigation menu */
  .sidenav {
    height: 100%; /* 100% Full-height */
    width: 0; /* 0 width - change this with JavaScript */
    position: fixed; /* Stay in place */
    z-index: 2000; /* Stay on top */
    top: 0;
    left: 0;
    box-shadow: 10px 0 10px rgba(0, 0, 0, 0.712);
    background-color: #152749;
    overflow-x: hidden; /* Disable horizontal scroll */
    padding-top: 60px; /* Place content 60px from the top */
    transition: 0.5s; /* 0.5 second transition effect to slide in the sidenav */
  }

  /* The navigation menu links */
  .sidenav div > :global(a) {
    padding: 8px 8px 8px 32px;
    text-decoration: none;
    font-size: 25px;
    color: #b6b6b6;
    display: block;
    transition: 0.3s;
  }

  /* When you mouse over the navigation links, change their color */
  .sidenav div > :global(a:hover) {
    color: #ffffff;
  }

  .opened {
    width: 200px;
  }

@media only screen and (max-width: 1480px){
  .menu :global(a) {
    color: white;
    text-decoration: none;
    font-size: 1rem;
    transition: 0.5s;
  }
  
}


@media only screen and (max-width: 1120px){
  .menu {
      display: none;
    }
  
}
  /* On smaller screens, where height is less than 450px, change the style of the sidenav (less padding and a smaller font size) */
  @media only screen and (max-width: 768px) {
    
    .menu :global(a) {
      display: none;
    }
    .sidenav {
      padding-top: 15px;
    }
    .sidenav div > :global(a) {
      font-size: 18px;
    }
    .logo img {
      width: 50px;
    }

    nav {
      height: 90px;
    }
  }
</style>
