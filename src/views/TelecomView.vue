<template>
  <header-bar></header-bar>
  <div class="kozah">
    <div class="header">
      <h1 class="titre">
        Télécommunications
      </h1>
    </div>

    <div class="bread">
      <nav
        style="--bs-breadcrumb-divider: url(&#34;data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='8' height='8'%3E%3Cpath d='M2.5 0L1 1.5 3.5 4 1 6.5 2.5 8l4-4-4-4z' fill='%236c757d'/%3E%3C/svg%3E&#34;);"
        aria-label="breadcrumb">
        <ol class="breadcrumb">
          <li class="breadcrumb-item"><a id="a" href="/about">Acommodation</a></li>
          <li class="breadcrumb-item active" aria-current="page">Télécommunications</li>
        </ol>
      </nav>
    </div>


    <div class="list-hotel">

      <h1>Les Télécommunications</h1>

      <div class="header-search">
        <form class="d-flex" role="search">
          <input class="form-control me-2" type="search" placeholder="Recherche" aria-label="Search">
          <button class="btn btn-outline-success" type="submit">Recherche</button>
        </form>
      </div>

      <div class="row">
        <div class="col-lg-6">
          <div class="card" style="width: 25rem; height: 32rem;">
            <img src="../components/images/telecom.jpg" class="card-img-top" alt="...">
            <div class="card-body">
              <h3 class="card-title">Agence moov Kara
              </h3>
              <p class="card-text"><b>Contact:</b> 96000000
              </p>
              <a type="button" class="btn btn-success" href="">Aller sur Place <i
                  class="icons fa-solid fa-location-dot"></i></a>

              <hr class="style-two">
            </div>
          </div>
        </div>



        <div class="col-lg-6">
          <div class="card" style="width: 25rem; height: 32rem;">
            <img src="../components/images/telecom.jpg" class="card-img-top" alt="...">
            <div class="card-body">
              <h3 class="card-title">Agence Togocel Kara</h3>
              <p class="card-text"><b>Contact:</b> 90000000
              </p>
              <a type="button" class="btn btn-success" href="">Aller sur Place <i
                  class="icons fa-solid fa-location-dot"></i></a>

              <hr class="style-two">
            </div>
          </div>
        </div>

      </div>











    </div>



  </div>
</template>

<script>
  import HeaderBar from '@/components/partials/HeaderBar.vue'
  export default {
    components: {
      HeaderBar
    }
  }
</script>

<style scoped>
  .col-lg-4:hover {
    transform: translateY(35px);
    transition: 1s ease-in-out;
  }

  .btn {
    text-decoration: none;
    border-radius: 13px;
    font-size: 10px;


  }

  .col-lg-3:hover {
    transform: translateY(35px);
    transition: 1s ease-in-out;
  }

  .bread {
    padding: 2rem;

  }

  #a {
    color: #006A4A;
  }

  ol {
    font-size: 20px;
  }

  a {
    text-decoration: none;
    color: #ffcc00;
    font-weight: bold;
    font-family: 'Josefin Sans', sans-serif;
  }

  .icon {
    color: red;
  }

  h2 {
    font-size: 15px;
  }

  .box1 {
    max-width: 18rem;
    text-align: center;
    border-radius: 25px;
    border: 2px solid red;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.26);
    margin-top: 2rem;
  }

  h3,
  p {
    font-size: 15px;
    font-family: 'jost', sans-serif;
    color: #006A4A;
    text-align: left;
  }

  .yellow-box {
    border: 2px solid yellow;
    padding: 1rem;
  }

  hr.style-two {
    border: 10px solid #006A4A;
    border-radius: 15px;
    background-color: #006A4A;
    width: 50%;
    margin-top: 4rem;



  }

  hr {
    background-color: #006A4A;
  }

  .row {
    padding: 1rem;
  }

  .list-pub {
    max-width: 100rem;
    height: 100%;
    text-align: center;
    border-radius: 25px;
    border: 2px solid yellow;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.26);
    padding: 3rem;
    background-color: white;
    margin: 1rem;
  }

  .card-img-top {
    border-radius: 15px;
    height: 200px;
  }

  .card {
    border-radius: 20px;
    max-width: 100%;
    text-align: center;
    border-radius: 22px;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
  }

  .card-title {
    text-align: left;
    color: #006A4A;
    text-transform: uppercase;
    font-size: 15px;
  }

  h1 {
    text-align: center;
    color: #006A4A;
    text-transform: uppercase;
    padding: 1rem;
    font-size: 30px;
  }



  .card-title {
    text-align: left;
    color: #006A4A;
    text-transform: uppercase;
    font-size: 15px;
  }

  h5 {
    color: red;
    text-align: left;
    font-size: 15px;
  }

  .card-text {
    text-align: left;
    color: #006A4A;

  }

  .list-hotel {
    background-image: linear-gradient(to right, #006a4a85, #ffcc00e6);
    padding: 3rem;
  }

  .header {
    height: 30vh;
    background-image:
      url(../components/images/banner.jpg);
    background-size: cover;
    background-position: top;
    position: relative;


  }


  .titre {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    text-align: center;
    color: #fff;
    /* animation: moveInRight 10s ease-out;
    animation-name: moveInLeft;
    animation-duration: 10s;
    animation-timing-function: ease-in; */
    font-weight: bold;
    font-size: 50px;
  }


  @keyframes moveInLeft {
    0% {
      opacity: 0;
      transform: translateX(-100px);
    }


    80% {
      transform: translateX(10px);
    }


    100% {
      opacity: 1;
      transform: translate(0) rotate(180deg);
    }
  }



  @keyframes moveInRight {
    0% {
      opacity: 0;
      transform: translateX(100px) rotate(0deg);
    }

    80% {
      transform: translateX(-20px);
    }

    100% {
      opacity: 1;
      transform: translate(0);
    }
  }

  @keyframes moveInBottom {
    0% {
      opacity: 0;
      transform: translateY(30px);
    }

    100% {
      opacity: 1;
      transform: translate(0);
    }
  }
</style>