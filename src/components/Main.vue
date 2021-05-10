<template>
  <div id="seccion-programar">

  <div class="container">
          <div class="titulo-seccion text-center">
              <h2>¿Qué es el <span>GENTLEMAN PROGRAMMING?</span></h2>
          </div>
          <div class="row">
              
              <div class="col-xl-6" >
                  <div class="texto-programador text-center align-items: center">
                  <p>Es una comunidad conformada por <br> distintos programadores de habla <br> hispana de diferente nivel(Trainee,Junior y Senior) </p>
                  </div>
              </div>
              <div class="col-xl-6 d-flex align-items-center justify-content-center" >
                  <div class="bigote">
                 <img src="../assets/bigote.png" alt="bigote">
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
.texto-programador{
    margin-top: 5rem;
    border-right: 2px solid #D60073;
}
.texto-programador p{
    color: white;
    font-size: 3.7vh;
}
.bigote img{
    width: 25rem;
}

.titulo-seccion{
    padding-top: 10rem;
    font-family:'Lato', sans-serif;
}
.titulo-seccion h2{
    
    color: white;
    font-weight: 700;
}
.titulo-seccion span{
    color: #F977BC ;
    font-weight: 900;
}
#seccion-programar{
    min-height: 45vh;
    background-color:#040F20 ;
}
/* Media Queries */
@media screen and (max-width:1199px){
    .texto-programador{
        margin-top: 1rem;
        border-bottom: 2px solid #D60073;
        border-right: none;
        font-size: 1.3rem;
    }



.bigote img{
    width: 18rem;
}

}
@media screen and (min-width:1024px) and (max-width:1026px){

.titulo-seccion h2{
    font-size: 3rem;
}
.bigote img{
    width: 22rem;
}

}

</style>