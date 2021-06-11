<template>
  <div id="seccion-programar">

  <div class="container" id="comunidad1">
          <div class="titulo-seccion text-center">
              <h2>NUESTRA <span>COMUNIDAD</span></h2>
          </div>
          <div class="row">
              
              <div class="col-xl-6 text-center align-items: center" >
                  <div class="titulo-comunidad">
                  <p>Al unirte a nuestra comunidad en <br> discord podrás acceder a distintos <br> contenidos referente a la <br> programación que van desde: <br> Memes hasta cursos <span>gratis</span> <br>¿Qué esperas para unirte? </p>
                  </div>
              </div>
              <div class="col-xl-6 d-flex align-items-center justify-content-center" >
                  <div class="discord">
                 <img src="../assets/DiscordG.png" alt="bigote">
                  </div>
              </div>
          </div>
      </div>
       </div>
</template>

<script>
export default {

}
</script>

<style>
html{
    scroll-behavior: smooth;
}
.titulo-comunidad{
    margin-top: 5rem;
    border-right: 2px solid #D60073;
    padding-right: 6rem;
    
}
.titulo-comunidad p{
    color: #ffffff;
    font-size: 1.6rem;
    font-family:'Lato', sans-serif;
    font-weight: 400;
}
.titulo-comunidad span{
    color: #F977BC;
    font-weight: 900;
}

.discord img{
    padding-top: 1rem;
    width: 25rem;
    padding-left: 3rem;
}

#seccion-programar{
    min-height: 45vh;
    background-color:#040F20 ;
}
@media screen and (min-width:220px) and ( max-width: 800px){
    .titulo-comunidad p{
        font-size: 1.4rem;
    }
}
@media screen and (max-width:1199px){
    .titulo-comunidad{
        text-align: center;
        margin-top: 1rem;
        padding-right: 0;
        border-bottom: 2px solid #D60073;
        border-right: none;
        font-size: 0.4rem;
    }
    .discord img{

        padding-left: 0;
        width: 18rem;
    }
}
@media screen and (min-width:1024px) and (max-width:1026px){


.discord img{
    width: 22rem;
}

}
</style>

