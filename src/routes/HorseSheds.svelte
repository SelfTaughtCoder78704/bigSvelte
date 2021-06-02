
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
title="Horse Sheds"
bgPos="30% 30%"
 images={[
   
   {
     link: 'https://bigtexdemo.netlify.app/assets/horseshed/image.jpg',
     num: 1
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/horseshed/image.png',
     num: 2
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/horseshed/image1.jpg',
     num: 3
   },
   {
       link: "https://bigtexdemo.netlify.app/assets/horseshed/image2.jpg",
       num: 4
   },
   {
       link: "https://bigtexdemo.netlify.app/assets/horseshed/image3.jpg",
       num: 5
   },
   {
       link: "https://bigtexdemo.netlify.app/assets/horseshed/image4.jpg",
       num: 6
   },
   {
       link: "https://bigtexdemo.netlify.app/assets/horseshed/image5.jpg",
       num: 7
   },
   {
       link: "https://bigtexdemo.netlify.app/assets/horseshed/image6.jpg",
       num: 8
   },
    
    ]}
  mainImage="https://bigtexdemo.netlify.app/assets/horseshed/image3.jpg"
  />
  </div>
