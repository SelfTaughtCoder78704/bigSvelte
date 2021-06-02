
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
title="Carports"
bgPos="30% 30%"
 images={[
   
   {
     link: 'https://bigtexdemo.netlify.app/assets/carport/image.jpg',
     num: 1
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/carport/image4.jpg',
     num: 2
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/carport/image1.jpg',
     num: 3
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/carport/image2.jpg',
     num: 4
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/carport/image3.jpg',
     num: 5
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/carport/image5.jpg',
     num: 6
   },
    
    ]}
  mainImage="https://bigtexdemo.netlify.app/assets/carport/image1.jpg"
  />
  </div>
