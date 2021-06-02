
<script>
    import { fly } from 'svelte/transition';
    import Building from "../components/Building.svelte";
    import { onMount } from "svelte";

  onMount(() => {
    window.scrollTo(0, 0);
  });
</script>
<div
    in:fly="{{ x: -100, duration: 500, delay: 300 }}"
    out:fly="{{ x: -100, duration: 500 }}" 
    >
    <Building 
title="RV Covers"
bgPos="30% 30%"
 images={[
  
   {
     link: 'https://bigtexdemo.netlify.app/assets/rvcover/rv1.jpg',
     num: 1
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/rvcover/rv2.jpg',
     num: 2
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/rvcover/rv3.jpg',
     num: 3
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/rvcover/rv4.jpg',
     num: 4
   },
   
    
    ]}
  mainImage="https://bigtexdemo.netlify.app/assets/rvcover/rv3.jpg"
  />
  </div>
