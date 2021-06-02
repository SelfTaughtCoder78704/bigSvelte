
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
title="Barns"
bgPos="center"
 images={[
   
   {
     link: 'https://bigtexdemo.netlify.app/assets/metalbarn/metal0.jpg',
     num: 1
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/metalbarn/metal1.jpg',
     num: 2
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/metalbarn/metal2.jpg',
     num: 3
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/metalbarn/metal3.jpg',
     num: 4
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/metalbarn/metal4.jpg',
     num: 5
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/metalbarn/metal5.jpg',
     num: 6
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/metalbarn/metal6.jpg',
     num: 7
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/metalbarn/metal7.jpg',
     num: 8
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/metalbarn/metal8.jpg',
     num: 9
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/metalbarn/metal9.jpg',
     num: 10
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/metalbarn/metal10.jpg',
     num: 11
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/metalbarn/metal11.jpg',
     num: 12
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/metalbarn/metal12.jpg',
     num: 13
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/metalbarn/metal13.jpg',
     num: 14
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/metalbarn/metal14.jpg',
     num: 15
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/metalbarn/metal15.jpg',
     num: 16
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/metalbarn/metal16.jpg',
     num: 17
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/metalbarn/metal17.jpg',
     num: 18
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/metalbarn/metal18.jpg',
     num: 19
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/metalbarn/metal19.jpg',
     num: 20
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/metalbarn/metal20.jpg',
     num: 21
   },
    
    ]}
  mainImage="https://bigtexdemo.netlify.app/assets/metalbarn/metal2.jpg"
  />
  </div>
  
  
  
  
  
  
  