<script>
    import { Link } from "svelte-routing";
    export let toPage = '';
    export let buildingName = '';
    export let desc = '';
    export let preImage = '';
</script>

<div class="preCard">
    <div class="cardGroup">
        <div class="top">
            <img src={preImage} alt={buildingName} />
            <h3>{buildingName}</h3>
        </div>
        <div class="bot">
            <p>{desc}</p>
           <Link to={toPage}>Go To {buildingName}</Link>
        </div>
    </div>
</div>



<style>
    .preCard{
       
        width: 100%;
        height: 100%;
        
        display: flex;
        justify-content:center;
        align-items: center;
    }
    .preCard img {
        width: 100%;
        height: 300px;
        object-fit: cover;
    }

    .cardGroup{
        width: 100%;
        border: 1px solid black;
        padding: 10px;
    }

    
    .bot :global(a) {
        display: block;
        font-family: "Montserrat", sans-serif;
        text-decoration: none;
        font-size: 14px;
        font-weight: 600;
        padding: 10px 20px;
        background-color: #1e3666;
        color: white;
        transition: 0.5s;
        border: 4px solid white;
        text-align: center;
    }
    .bot :global(a:hover) {
        background: white;
        border-color: #1e3666;
        color: #1e3666;
    }

    @media only screen and (max-width: 768px) {
      .cardGroup {
          margin: 10px 0;
      }

    
    }
</style>