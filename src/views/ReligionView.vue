<template>
     <header-bar></header-bar>
     <div class="kozah">
          <div class="header">
               <h1 class="titre">
                    Lieux Religieux
               </h1>
          </div>

          <div class="bread">
               <nav style="--bs-breadcrumb-divider: url(&#34;data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='8' height='8'%3E%3Cpath d='M2.5 0L1 1.5 3.5 4 1 6.5 2.5 8l4-4-4-4z' fill='%236c757d'/%3E%3C/svg%3E&#34;);"
                    aria-label="breadcrumb">
                    <ol class="breadcrumb">
                         <li class="breadcrumb-item"><a href="/about">Acommodation</a></li>
                         <li class="breadcrumb-item active" aria-current="page">Lieux Religieux</li>
                    </ol>
               </nav>
          </div>


          <div class="list-hotel">

               <h1>Les Lieux Religieux</h1>
               <div class="header-search">
                    <form class="d-flex" role="search">
                         <input class="form-control me-2" type="search" placeholder="Recherche" aria-label="Search">
                         <button class="btn btn-outline-success" type="submit">Recherche</button>
                    </form>
               </div>


               <div class="row" v-if="religion && religion.length">
                    <div class="col-lg-4" v-for="reg of religion" :key="reg.id">
                         <div class="card" style="width: 25rem; height: 30rem;">
                              <img :src="'http://karaevents.mekengroup.com/upload/lieu_religieu/'+reg.photo_lieu_religieux"
                                   class="card-img-top" alt="...">
                              <div class="card-body">
                                   <h3 class="card-title">{{ reg.nom_lieu_religieux}}</h3>
                                   <br>
                                   <a type="button" class="btn btn-success"
                                        :href="'https://goo.gl/maps/'+reg.localisation_lieu_religieux"
                                        target="blank">Aller sur Place <i
                                             class="icons fa-solid fa-location-dot"></i></a>

                              </div>
                         </div>
                    </div>
               </div>



          </div>

          <div class="arrow">


               <div style="text-align:">
                    <a href="/marche" type="button" class="btn btn-outline-success"><i
                              class="fa-solid fa-arrow-left"></i>
                         Previous</a>
               </div>
               <div style="text-align:">
                    <a href="/gym" type="button" class="btn btn-outline-success">Next <i
                              class="fa-solid fa-arrow-right"></i></a>
               </div>


          </div>



     </div>
</template>

<script>
     import HeaderBar from '@/components/partials/HeaderBar.vue'
     import axios from 'axios'
     export default {
          components: {
               HeaderBar
          },

          data() {
               return {
                    religion: [],
                    errors: []
               }
          },

          // Fetches posts when the component is created.
          created(data) {
               axios.get(`api/lieu_religieu`)
                    .then(response => {
                         // JSON responses are automatically parsed.
                         this.religion = response.data
                         console.log(data)

                    })
                    .catch(e => {
                         this.errors.push(e)
                    })
          }



     }
</script>

<style scoped>
     .bread {
          padding: 2rem;

     }

     .btn {
          text-decoration: none;
          border-radius: 13px;
          font-size: 12px;


     }

     ol {
          font-size: 20px;
     }

     a {
          text-decoration: none;
          font-weight: bold;
          font-family: 'Josefin Sans', sans-serif;
     }

     .arrow {
          padding: 4rem;
          display: flex;
          justify-content: space-between;
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
          border-radius: 10px;
     }

     .card {
          border-radius: 10px;
          max-width: 100%;
          text-align: center;
          box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
     }

     .card-title {
          text-align: left;
          color: #006A4A;
          text-transform: uppercase;
          font-size: 20px;
     }

     h1 {
          text-align: center;
          color: #006A4A;
          text-transform: uppercase;
          padding: 1rem
     }

     ;

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