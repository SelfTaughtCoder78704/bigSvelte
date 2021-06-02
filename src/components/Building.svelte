<script>
  export let images = [];
  export let title = "building";
  export let mainImage = "";
  export let bgPos = "";
  let modalImage = "";
  let modalNum = 0;
  let modalOpen = false;
  const openModal = (e) => {
    if (e.target != document.querySelector(".look")) {
      modalOpen = !modalOpen;
      modalImage = e.target.src;
      modalNum = e.target.getAttribute("data-num");
    }
  };
</script>

<div
  class="bannerBox"
  style="background-image: url('{mainImage}'); background-position: {bgPos}; background-repeat: no-repeat; background-size: cover;"
>
  <div class="overlay2">
    <h1>{title}</h1>
  </div>
</div>
<div class="building">
  <!-- <img class="mainImg" src={mainImage} alt={title + ' building'}/> -->
  <ul class="imgGrid">
    {#each images as image}
      <li>
        <img
          data-num={image.num}
          on:click={openModal}
          src={image.link}
          alt={title + " building"}
        />
        <div class="overlay"><p>{image.num}</p></div>
      </li>
    {/each}
  </ul>
</div>

<div
  id="myModal"
  class="modal"
  on:click={openModal}
  class:modalIsOpen={modalOpen}
>
  <div class="modal-content">
    <span class="close">&times;</span>
    <img class="lrgImg" src={modalImage} alt={title + " building"} />
    <p>
      To inquire about this style, either call <a
        class="look"
        href="tel:+1-254-493-5094"
        >254-493-5094
      </a>
      and mention <span class="look">{title} 	&#35;{modalNum}</span> or fill out our
      quote form and mention <span class="look">{title} 	&#35;{modalNum}</span> in your message.
    </p>
  </div>
</div>

<style>
  .overlay2 {
    margin: 1em auto;
    width: 100%;
    height: 100%;
    /* height: 500px; */
    padding: 50px 0;
    display: flex;
    justify-content: center;
    align-items: center;
    background: rgba(0, 0, 0, 0.4);
    margin-bottom: 1em;
  }
  .bannerBox {
    width: 90%;
    margin: 0 auto;
    
  }
  
  .lrgImg {
    width: 100%;
    height: 500px;
    object-fit: cover;
  }
  .building {
    width: 70%;
    margin: 0 auto;
    padding-bottom: 200px;
    cursor: pointer;
  }
  h1 {
    text-align: center;
    color: white;
    font-size: 72px;
  }
  
  .imgGrid {
    width: 100%;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, auto));
    grid-gap: 1em;
    list-style: none;
    margin: 0;
    padding: 0;

  }
  li {
    width: 100%;
    height: 100%;
    position: relative;
    
  }

  .imgGrid img {
    width: 100%;
    height: 350px;
    object-fit: cover;
  }

  .overlay {
    pointer-events: none;
    width: 100%;
    height: 100%;
    background: linear-gradient(135deg, rgba(0, 0, 0, 0) 60%, #1d3565 100%);
    position: absolute;
    top: 0;
    left: 0;
  }

  .overlay p {
    font-size: 42px;
    color: rgb(255, 255, 255);
    position: absolute;
    bottom: 0;
    padding: 0;
    margin: 0;
    right: 10px;
  }

  /* The Modal (background) */
  .modal {
    display: none; /* Hidden by default */
    position: fixed; /* Stay in place */
    z-index: 2001; /* Sit on top */
    left: 0;
    top: 0;
    width: 100%; /* Full width */
    height: 100%; /* Full height */
    overflow: auto; /* Enable scroll if needed */
    background-color: rgb(0, 0, 0); /* Fallback color */
    background-color: rgba(0, 0, 0, 0.4); /* Black w/ opacity */
  }

  /* Modal Content/Box */
  .modal-content {
    background-color: #fefefe;
    margin: 5% auto; /* 15% from the top and centered */
    padding: 20px;
    border: 1px solid #888;
    text-align: center;
    width: 50%; /* Could be more or less, depending on screen size */
  }

  .modal-content p {
    width: 70%;
    font-size: 20px;
    margin: 20px auto;
  }

  .look {
    color: red;
    text-transform: uppercase;
    font-style: italic;
    font-weight: bold;
    font-size: 20px;
  }

  /* The Close Button */
  .close {
    color: #aaa;
    float: right;
    font-size: 28px;
    font-weight: bold;
  }

  .close:hover,
  .close:focus {
    color: black;
    text-decoration: none;
    cursor: pointer;
  }

  .modalIsOpen {
    display: block;
  }

  @media only screen and (max-width: 768px) {
    /* .modal {
      height: auto;
    } */

    .modal-content img {
      height: 300px;
    }
    
    .modal-content {
      width: 90%;
      padding: 10px;
    }
    .building {
      width: 90%;
    }
    .bannerBox {
      height: 200px;
    }

    h1 {
    font-size: 2rem;
  }
  .overlay2{
    padding: 20px 0;
  }
  .bannerBox {
    height: auto;
    
  }
  .modal-content p {
    font-size: 12px;
    padding: 5px ;
    width: 100%;
  }

  .look {
    
    font-size: 14px;
  }
  
  }
</style>
