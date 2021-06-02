<script>
    import { fly } from "svelte/transition";
    import { Link } from "svelte-routing";
    import Flags from "../components/Flags.svelte";
    import { onMount } from "svelte";

  onMount(() => {
    window.scrollTo(0, 0);
  });
</script>

<svelte:head>
    <link rel="preconnect" href="https://fonts.gstatic.com" />
    <link
        href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;600;900&display=swap"
        rel="stylesheet"
    />
</svelte:head>
<div
    in:fly={{ x: -100, duration: 500, delay: 300 }}
    out:fly={{ x: -100, duration: 500 }}
>
    <main>
        <div class="overlayDiv ">
            <div class="homeTagLine">
                <h1>Big Tex <br /> <span>Metal Buildings</span></h1>
                <button id="viewBuildingsBtn"
                    ><Link to="/all-buildings">View Buildings</Link></button
                >
                <button id="viewBuildingsBtn2"
                    ><Link to="/quote">Get A Quote</Link></button
                >
            </div>
        </div>
    </main>
    <div id="underMain">
        <p class="tagLine">
            Welcome To The Home Of Quality Metal Buildings! We Not Only Offer
            Galvanized Metal Buildings, But We Also Install Red Iron Metal
            Buildings.
        </p>
        <Flags />
        
    </div>
</div>

<style>
    .homeTagLine {
        padding: 0;
        margin: 0;
    }
    .tagLine {
        width: 70%;
        margin: 20px auto;
        font-size: 36px;
        color: #1e3666;
        font-weight: 700;
        line-height: 56px;
        font-family: "Montserrat", sans-serif;
    }

    #viewBuildingsBtn :global(a) {
        text-decoration: none;
        color: white;
    }
    #viewBuildingsBtn2 :global(a) {
        text-decoration: none;
        color: white;
    }
    #viewBuildingsBtn:hover :global(a) {
        color: #1e3666;
    }

    #viewBuildingsBtn2:hover :global(a) {
        color: #8f3a3d;
    }
    main {
        width: 100%;
        background: url(https://bigtexdemo.netlify.app/assets/metalbarn/metal14.jpg)
            no-repeat;
        background-size: cover;
        background-position: center;
        background-attachment: fixed;
    }

    .overlayDiv {
        width: 100%;
        height: 100vh;
        background: linear-gradient(to right, #152749, #1e3666e3);
        display: flex;
        justify-content: center;
        align-items: center;
    }
    .overlayDiv div {
        text-align: center;
        width: 70%;
        margin: 0 auto;
    }
    h1 {
        color: #ffffff;
        line-height: 72px;
        font-size: 90px;
        font-family: "Montserrat", sans-serif;
        font-weight: 900;
        padding: 0;
        margin: 0;
        margin-bottom: 30px;
        text-transform: uppercase;
    }

    h1 span {
        font-size: 80px;
        /* color: #8F3A3D; */
    }

    #viewBuildingsBtn {
        max-width: 400px;
        font-family: "Montserrat", sans-serif;

        font-size: 24px;
        font-weight: 900;
        padding: 20px 40px;
        background-color: #8f3a3d;
        color: white;
        /* border-radius: 50px; */
        transition: 0.5s;
        border: 4px solid white;
    }

    #viewBuildingsBtn2 {
        max-width: 400px;
        font-family: "Montserrat", sans-serif;
        margin-left: 20px;
        font-size: 24px;
        font-weight: 900;
        padding: 20px 40px;
        background-color: #1e3666;
        color: white;
        /* border-radius: 50px; */
        transition: 0.5s;
        border: 4px solid white;
    }

    #viewBuildingsBtn:hover {
        background: white;
        border-color: #1e3666;
        color: #1e3666;
    }

    #viewBuildingsBtn2:hover {
        background: white;
        border-color: #8f3a3d;
        color: #8f3a3d;
    }

    #underMain {
        padding-top: 50px;
        padding-bottom: 200px;
        width: 100%;
        margin: 0 auto;
        background: white;
        /* padding: 50px 0; */
        text-align: center;
    }

    @media only screen and (max-width: 768px){
        h1 {
            line-height: 2.8rem;
            font-size: 3rem;
            margin: 0;
        }

        h1 span {
            font-size: 2rem;
            /* color: #8F3A3D; */
            line-height: 1.8rem;
        }

        #viewBuildingsBtn2, #viewBuildingsBtn{
            font-size: 14px;
            margin: 10px auto;
        }

        .tagLine {
        width: 80%;
        margin: 20px auto;
        font-size: 1.3rem;
        color: #1e3666;
        font-weight: 700;
        line-height: 1.6rem;
        font-family: "Montserrat", sans-serif;
    }
    #underMain{
        padding-top: 20px;
        padding-bottom: 50px;
    }
    }
</style>
