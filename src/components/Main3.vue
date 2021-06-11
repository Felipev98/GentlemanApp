<template>
  <div id="seccion-youtube">

  <div class="container" id="Youtube">
          <div class="titulo-seccion text-center">
              <h2>¿CÓMO EMPIEZO A <span>PROGRAMAR?</span></h2>
          </div>
          <div class="row">
              
              
              <div class="col-xl-6 text-center align-items: center" >
                  <div class="titulo-comunidad">
                <p>¿No sabes por dónde empezar? <br> ¡Tranquilo! Tenemos una serie de <br> videos que van desde lo básico en <br> programación hasta nivel experto.</p>
                    <router-link id="boton-youtube" to="/Youtube">Empieza a programar</router-link>
             
                  </div>
                 
              </div>      
              <div class="col-xl-6 d-flex align-items-center justify-content-center" >
                  <div class="youtube">
                 <img src="../assets/programar.png" alt="bigote">
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

.titulo-seccion p{
    color: white;
    font-size: 1.6rem;
    font-family:'Lato', sans-serif;
    font-weight: 400;
}
.boton-youtube{
    border-radius: 1rem;
    background-color: #D60073;
    transform: translateX(180%);
    line-height: 1rem;

}


.youtube img{
    padding-top: 1rem;
    width: 25rem;
    padding-left: 3rem;
}

#seccion-youtube{
    min-height: 100vh;
    background-color:#040F20 ;
}
.boton-contenedor{
    display: flex;
    justify-content: flex-start;
}
#boton-youtube{
    padding: 0.7rem;
    background-color: #D60073;
    margin-bottom: 1rem;
    text-align: center;
    font-size: 1.2rem;
    width: 40%;
    font-family: 'Lato', sans-serif;
    font-weight: 700;
    border-radius: 1rem;
    text-align: center;
    cursor: pointer;
    transition: all 0.3s ease;
    color: white;
    transform: translateX(80%);
    text-decoration: none;
    display: flex;
    justify-content: center;
    
}
#boton-youtube:hover{
    background-color: fuchsia;

}
/* Media Queries */
@media screen and (max-width:1199px){
    .titulo-comunidad{
        text-align: center;
        margin-top: 3rem;
        padding-right: 0;
        border-bottom: 2px solid #D60073;
        border-right: none;
        font-size: 10rem;
    }
    .titulo-seccion p{
        font-size: 80rem;
    }    

    #boton-youtube{
        margin-top: 2rem;
        width: 20%;
        transform: translateX(200%);
    }
 .youtube img{
     padding-left: 0;
     margin-top: 8rem;
     width: 18rem
     
 }
}
@media screen and (min-width:800px) and (max-width:1023px){

#unirme{
    font-size: 1.5rem  !important;
}
}

@media screen and (min-width:1024px) and (max-width:1090px){


.youtube img{
    width:22rem;
}

#boton-youtube{
    font-size: 1.4rem;
}
#seccion-youtube{
    min-height: 60vh;
}
#unirme{
    font-size: 1.5rem !important;
}

}
@media screen and (max-width:600px) { 
    #boton-youtube{ width: 50%; 
    transform: translateX(50%); 
    } 
 }
 .youtube img{
     margin-top:3rem;
 }

</style>
