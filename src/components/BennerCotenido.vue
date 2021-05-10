<template>
<div class="full-height" id="banner">
  <b-navbar toggleable="lg" type="dark" variant="info">
      <b-container>
    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
    <b-navbar-brand href="#" class=""> <img src="../assets/logo.png" alt=""></b-navbar-brand>
        <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav class="mx-auto">
        <b-nav-item href="#InicioSección" class="navbar">Inicio</b-nav-item>
        <b-nav-item href="#Youtube" class="navbar" >Youtube</b-nav-item>
        <b-nav-item href="#comunidad1" id="comunidad" >Comunidad</b-nav-item>
      </b-navbar-nav>
          </b-collapse>
      </b-container>
        </b-navbar>


<div class="container" id="InicioSección">
    <div class="row ">
        <div class="col-xl-6 align-items-center " id="banner-imagen" >
            <h2>APRENDE A PROGRAMAR <br>COMO UN <span>GENTLEMAN</span> </h2>
            <p>Unete a una comunidad de programadores de habla <br>hispana y conviertete en un "pro" de la programación</p>
                <a href="#comunidad1" id="unirme">¡Unirme ya!</a>
            

        </div>
         <div class="col-xl-6  " id="lol">
            <img src="../assets/lol.png" alt="alan">
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

<style scoped>

html{
    scroll-behavior: smooth;
}


#banner{
    background-image: url(../assets/Banner.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    overflow: hidden;
    background-attachment: fixed;
}
.navbar .navbar-brand{
    height: 4rem;
}
.navbar .navbar-brand img{
    width: 4.5rem;
}

.navbar .nav-item a{
    margin: 0;
    padding: 0;
}

.navbar{
    margin-left: 1rem;
}

#comunidad{
    padding: 0.7rem;
    background-color: #EA1889;
    border-radius: 1rem;
    box-shadow: 0px 1px 8px #EA1889;
    font-size: 1rem;
    color: white;
    font-family: 'Lato', sans-serif;
    font-weight: 400;
    transition: all 0.3s ease ;
    font-size: 1rem;
    margin-right: 0;
}
#comunidad:hover{
    transform: scale(1.2);

}
#comunidad a:hover{
color:  white !important;

}
.nav-link{
  margin-left: 2rem;

}
.navbar {
    background-color: transparent !important;
 }
.navbar .nav-item a{
    color: white;
    font-family: 'Lato', sans-serif;
    font-weight: 400;
    transition: all 0.3s ease ;
    font-size: 1rem;

}
.navbar .nav-item a:hover{
    color: #EA1889;
}

#banner-imagen{
    padding-top: 15vw;
}
#banner-imagen h2{
    font-family: 'Poppins', sans-serif;
    font-size: 6.2vh ;
    color: white;
    font-weight: 700;
}
#banner-imagen h2 span{
    color: #F977BC;
    font-weight: 900;
}
#banner-imagen p{
    color: #DFDFDF;
    font-family: 'Lato', sans-serif;
    font-size: 2.5vh;
}
#unirme{
    padding: 0.9rem;
    background-color: #D60073 ;
    border-radius: 1rem;
    width: 25%;
   text-decoration: none;
    color: white;
    font-family: 'Lato', sans-serif;
    font-size: 1.2rem;
    font-weight: 700;
    box-shadow: 0px 1px 8px #EA1889;
    transition: all 0.3s ease;
    text-align: center;
    }

    #unirme:hover{
        background-color: fuchsia;
    }
 #lol img{
     width: 34rem;
  padding-top: 15vh;
   
 }


/* Media Queries */
@media screen and (min-width:1300px){

#lol img{
padding-top: 10rem;
}
#banner-imagen{
    padding-top: 12vw;
}

}
@media screen and (max-width:1199px){

#lol img{
    padding: 0;
    width: 14rem;
    justify-content: center;
    transform: translateX(40%);

}


@media screen and (max-width:460px){
#unirme{
    transform: translateX(40%);
    width: 40%;
    justify-content: center;
}
#lol img{
transform: translateX(16.5%);
justify-content: center;

}
}

}
@media screen and (max-width:992px){
.navbar .nav-item   {
    padding:0;

}

#comunidad{
    background-color: transparent;
    box-shadow: inherit;
}

#comunidad:hover{
    transform: none;
    background-color: transparent;
}

}
#nav-collapse{
    background-color: #D60073;
}
#nav-collapse a{
    padding: 1rem;
}

@media screen and (min-width:994px){
    #nav-collapse{
        background-color: inherit;
        padding: 1rem;
        margin: 0;

    }
    #nav-collapse a{
        padding: 0rem;
    }
    
}
</style>
