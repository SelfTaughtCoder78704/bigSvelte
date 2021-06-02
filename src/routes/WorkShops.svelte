
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
title="Workshops"
bgPos="30% 30%"
 images={[
   
   {
     link: 'https://bigtexdemo.netlify.app/assets/workshop/image.jpg',
     num: 1
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/workshop/image1.jpg',
     num: 2
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/workshop/image2.jpg',
     num: 3
   },
   {
       link: "https://bigtexdemo.netlify.app/assets/workshop/image3.jpg",
       num: 4
   },
   {
       link: "https://bigtexdemo.netlify.app/assets/workshop/image4.jpg",
       num: 5
   },
   {
       link: "https://bigtexdemo.netlify.app/assets/workshop/image5.jpg",
       num: 6
   },
   {
       link: "https://bigtexdemo.netlify.app/assets/workshop/image6.jpg",
       num: 7
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/workshop/image7.jpg',
     num: 8
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/workshop/image8.jpg',
     num: 9
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/workshop/image9.jpg',
     num: 10
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/workshop/image10.jpg',
     num: 11
   },
   {
       link: "https://bigtexdemo.netlify.app/assets/workshop/image11.jpg",
       num: 12
   },
   {
       link: "https://bigtexdemo.netlify.app/assets/workshop/image12.jpg",
       num: 13
   },
   {
       link: "https://bigtexdemo.netlify.app/assets/workshop/image13.jpg",
       num: 14
   },
   {
       link: "https://bigtexdemo.netlify.app/assets/workshop/image14.jpg",
       num: 15
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/workshop/image15.jpg',
     num: 16
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/workshop/image16.jpg',
     num: 17
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/workshop/image17.jpg',
     num: 18
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/workshop/image18.jpg',
     num: 19
   },
   {
       link: "https://bigtexdemo.netlify.app/assets/workshop/image19.jpg",
       num: 20
   },
   {
       link: "https://bigtexdemo.netlify.app/assets/workshop/image20.jpg",
       num: 21
   },
   {
       link: "https://bigtexdemo.netlify.app/assets/workshop/image21.jpg",
       num: 22
   },
   {
       link: "https://bigtexdemo.netlify.app/assets/workshop/image22.jpg",
       num: 23
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/workshop/image23.jpg',
     num: 24
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/workshop/image24.jpg',
     num: 25
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/workshop/image25.jpg',
     num: 26
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/workshop/image26.jpg',
     num: 27
   },
   {
       link: "https://bigtexdemo.netlify.app/assets/workshop/image27.jpg",
       num: 28
   },
   {
       link: "https://bigtexdemo.netlify.app/assets/workshop/image28.jpg",
       num: 29
   },
   {
       link: "https://bigtexdemo.netlify.app/assets/workshop/image29.jpg",
       num: 30
   },
   {
       link: "https://bigtexdemo.netlify.app/assets/workshop/image30.jpg",
       num: 31
   },
   {
       link: "https://bigtexdemo.netlify.app/assets/workshop/image31.jpg",
       num: 32
   },
   {
       link: "https://bigtexdemo.netlify.app/assets/workshop/image32.jpg",
       num: 33
   },
   {
       link: "https://bigtexdemo.netlify.app/assets/workshop/image33.jpg",
       num: 34
   },
   
    
    ]}
  mainImage="https://bigtexdemo.netlify.app/assets/workshop/image21.jpg"
  />
  </div>
