
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
title="Patio Covers"
bgPos="20% 20%"
 images={[
   
   {
     link: 'https://bigtexdemo.netlify.app/assets/patio/image4.jpg',
     num: 1
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/patio/image3.jpg',
     num: 2
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/patio/image2.jpg',
     num: 3
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/patio/image.jpg',
     num: 4
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/patio/image1.jpg',
     num: 5
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/patio/image6.jpg',
     num: 6
   },
    
    ]}
  mainImage="https://bigtexdemo.netlify.app/assets/patio/image1.jpg"
  />
  </div>
  