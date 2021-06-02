<script>
    export let num = ''
</script>

<a href="tel:+1{num}" class="phoneIcon">&phone;</a>

<style>
    .phoneIcon{
        position: fixed;
        bottom: 65px;
        right: 20px;
        z-index: 2001;
        background: rgb(52, 230, 16);
        color: rgb(0, 0, 0);
        border-radius: 100%;
        width: 40px;
        height: 40px;
        display: flex;
        justify-content:center;
        align-items: center;
        cursor: pointer;
        text-decoration: none;
        font-size: 1.3rem;
        transition: all 0.5s ease;
  
    }

    .phoneIcon:hover {
        background: red;
        color: white;
        width: 70px;
        height: 70px;
        font-size: 3rem;
        box-shadow: 0 0 20px rgba(0, 0, 0, 0.6);
    }

    @media only screen and (max-width: 768px){
        .phoneIcon {
            bottom: 28px;
            right: 2px;
        }
    }
</style>