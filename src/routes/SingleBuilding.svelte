
<script>
    
    import Building from "../components/Building.svelte";
    import { onMount } from "svelte";

  onMount(() => {
    window.scrollTo(0, 0);
  });
</script>

<Building 
title="Carports"
 images={[
   {
     link: 'https://bigtexdemo.netlify.app/assets/carport/image.jpg',
     num: 1
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/carport/image1.jpg',
     num: 2
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/carport/image.jpg',
     num: 3
   },
   {
     link: 'https://bigtexdemo.netlify.app/assets/carport/image.jpg',
     num: 4
   },
    
    ]}
  mainImage="https://bigtexdemo.netlify.app/assets/carport/image5.jpg"
  />