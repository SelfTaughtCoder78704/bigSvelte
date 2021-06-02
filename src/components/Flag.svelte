<script>
    import { Link } from "svelte-routing";
    export let title = "";
    export let toPlace = "";
    export let pic = "";
    export let imageOfFlag = "";
</script>

<div class="flag">
    <Link to={toPlace}>
        <div>
            <img src={pic} alt={title} />
            <img src={imageOfFlag} alt={title + " flag"} />
        </div>
    </Link>
</div>

<style>
    .flag {
        width: 100%;
        transition: 0.5s;
        padding: 20px 5px;
        display: flex;
        justify-content: center;
        align-items: center;
        background: #152749;
        /* padding: 20px; */
    }

    .flag:hover {
        background: radial-gradient(
            rgb(255, 238, 0) 0%,
            rgba(255, 255, 255, 0) 100%
        );
        /* box-shadow: 10px 10px 20px rgba(0, 0, 0, 0.6) */
    }
</style>
