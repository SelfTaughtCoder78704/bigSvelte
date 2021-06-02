<script>
    import Nav from "./components/Nav.svelte";
    import Footer from './components/Footer.svelte';
    import CallBtn from './components/CallBtn.svelte';
    
    
  </script>
  
  <svelte:body/>
  <div class="wrap">
    <Nav />
  <CallBtn num="2544935094" />
  <Footer />
  </div>
  <style>
    :global(body) {
      margin: 0;
      padding: 0;
    }

    .wrap{
      width: 100%;
      position: relative;
    }
  </style>
  
  