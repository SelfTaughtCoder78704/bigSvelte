<script>
    import Flag from "./Flag.svelte";
</script>

<div class="flags">
    <Flag
        title="Barns"
        toPlace="/barns"
        pic="https://bigtexdemo.netlify.app/assets/demos/barnDemo.png"
        imageOfFlag="https://bigtexdemo.netlify.app/assets/flags/barnFlag.png"
    />
    <Flag
        title="RV Covers"
        toPlace="/rv-covers"
        pic="https://bigtexdemo.netlify.app/assets/demos/roundDemo.png"
        imageOfFlag="https://bigtexdemo.netlify.app/assets/flags/rvFlag.png"
    />
    <Flag
        title="Patio Covers"
        toPlace="/patio-covers"
        pic="https://bigtexdemo.netlify.app/assets/demos/patioSplash.png"
        imageOfFlag="https://bigtexdemo.netlify.app/assets/flags/patioFlag.png"
    />
    <Flag
        title="Red Iron Metal Buildings"
        toPlace="/red-iron-metal-buildings"
        pic="https://bigtexdemo.netlify.app/assets/demos/redIDemo.png"
        imageOfFlag="https://bigtexdemo.netlify.app/assets/flags/redFlag.png"
    />
    <Flag
        title="Workshops"
        toPlace="/workshops"
        pic="https://bigtexdemo.netlify.app/assets/demos/workDemo.png"
        imageOfFlag="https://bigtexdemo.netlify.app/assets/flags/workFlag.png"
    />
    <Flag
        title="Carports"
        toPlace="/carports"
        pic="https://bigtexdemo.netlify.app/assets/demos/carportsDemo.png"
        imageOfFlag="https://bigtexdemo.netlify.app/assets/flags/carportFlag.png"
    />
    <Flag
        title="Horse Sheds"
        toPlace="/horse-sheds"
        pic="https://bigtexdemo.netlify.app/assets/demos/horseDemo.png"
        imageOfFlag="https://bigtexdemo.netlify.app/assets/flags/horseFlag.png"
    />
    <Flag
        title="Lean Tos"
        toPlace="/lean-tos"
        pic="https://bigtexdemo.netlify.app/assets/demos/leanDemo.png"
        imageOfFlag="https://bigtexdemo.netlify.app/assets/flags/leantoFlag.png"
    />
    <Flag
        title="Concrete And More"
        toPlace="/concrete-and-more"
        pic="https://bigtexdemo.netlify.app/assets/demos/concDemo.png"
        imageOfFlag="https://bigtexdemo.netlify.app/assets/flags/concreteFlag.png"
    />
</div>

<style>
    .flags {
        width: 70%;
        margin: 40px auto;
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, auto));
        grid-gap: 1em;
        
    }
</style>
