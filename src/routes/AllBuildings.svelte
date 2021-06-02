<script>
    import BuildingPreview from '../components/BuildingPreview.svelte';
    import { onMount } from "svelte";

  onMount(() => {
    window.scrollTo(0, 0);
  });
</script>
<h1>All Building Types</h1>
<div class="gridded">
    <BuildingPreview preImage="https://bigtexdemo.netlify.app/assets/carport/image1.jpg" buildingName="Carports" toPage="/carports" desc="Vistit Carports to see styles" />
    <BuildingPreview preImage="https://bigtexdemo.netlify.app/assets/patio/image1.jpg" buildingName="Patio Covers" toPage="/patio-covers" desc="Vistit Patio Covers to see styles" />
    <BuildingPreview preImage="https://bigtexdemo.netlify.app/assets/rvcover/rv1.jpg" buildingName="RV Covers" toPage="/rv-covers" desc="Vistit RV Covers to see styles" />
    <BuildingPreview preImage="https://bigtexdemo.netlify.app/assets/metalbarn/metal6.jpg" buildingName="Barns" toPage="/barns" desc="Vistit Barns to see styles" />
    <BuildingPreview preImage="https://bigtexdemo.netlify.app/assets/leanto/image2.jpg" buildingName="Lean Tos" toPage="/lean-tos" desc="Vistit Lean Tos to see styles" />
    <BuildingPreview preImage="https://bigtexdemo.netlify.app/assets/horseshed/image3.jpg" buildingName="Horse Sheds" toPage="/horse-sheds" desc="Vistit Horse Sheds to see styles" />
    <BuildingPreview preImage="https://bigtexdemo.netlify.app/assets/rediron/image4.jpg" buildingName="Red Iron Metal Buildings" toPage="/red-iron-metal-buildings" desc="Vistit Red Iron Metal Buildings to see styles" />
    <BuildingPreview preImage="https://bigtexdemo.netlify.app/assets/workshop/image21.jpg" buildingName="Workshops" toPage="/workshops" desc="Vistit Workshops to see styles" />
    <BuildingPreview preImage="https://bigtexdemo.netlify.app/assets/carport/image1.jpg" buildingName="Carports" toPage="/carports" desc="Vistit Carports to see styles" />
    
</div>

<style>
h1{
  text-align: center;
}
    .gridded {
        width: 70%;
        margin: 100px auto;
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(350px, auto));
        grid-gap: 1em;
        padding-bottom: 50px;
    }

    @media only screen and (max-width: 768px) {
      .gridded {
        display: block;
        width: 90%;
      }

    
    }
</style>