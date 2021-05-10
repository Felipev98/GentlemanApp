<template>
 <div id="seccion-app">
   <router-link to="/" ><nav class="navbar"  >
  <img class="navbar-brand " src="../assets/logo.png" alt="logo">
</nav></router-link>

<div class="container">
  <div class="row">
    <div class="col-12 ">
    
              <h2>¡BUSCA EL CONTENIDO QUE <br> QUIERES APRENDER!</h2>
      </div>
      
    
  </div>
  


</div>

 </div>
</template>

<script>

export default {
  data() {
    return {
    }
  },

}
</script>

<style scoped >
.navbar .navbar-brand{
    height: 4rem;
}

.col-12{
  color: white;
  transform:translateY(30%);
  font-family: 'Lato', sans-serif;
  font-weight: 700;

}
.input-text{
  position: absolute;
  top: 5rem;
  border-radius: 0.8rem;
  width: 20rem;
  padding: 0.6rem;
  outline: none;
  border: none;
  box-shadow: 0px 1px 8px #EA1889 ;
  transition: 0.4s all ease-out;
}
.input-text:hover{
  box-shadow: 3px 3px 12px #EA1889;
  transform:scale(1.1);
}
#input-titulo{
  text-align: center;
}
::placeholder{
  color: #A8A8A8;
  font-family: 'Lato', sans-serif;
  font-size: 1rem;
}

/* Media Queries */
@media screen and (max-width:560px){
  .col-12 h2{
    font-size: 1.3rem;
  }
}

</style>