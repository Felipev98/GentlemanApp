<template>
<div>
    <Youtubenav/>
   <div class="container">
     <div class="input-container">
           <input type="text" class="input-text" name="Buscar" placeholder="Buscar contenido" v-model="search" v-on:keyup.enter="searchData">
           </div> 
   </div>
<div class="tarjetas-seccion">
<div class="row mx-5">
  <div class="col row grid">
    <div class="card mx-auto" style="width:27rem; margin-top:4.5rem"  v-for="video in videos" :video="video" :key="video.id.videoId" > 
      <img class="card-img-top"  :src="video.snippet.thumbnails.medium.url" alt="imagen">
      <div class="card-body">
        <b-card-text >
          <h6>{{video.snippet.title}}</h6>
      <p>{{video.snippet.description}}</p>
    </b-card-text>
    
    
    
   
  <b-modal :id="'myModal'+video.id.videoId" :title="video.snippet.title">
    <div class="iframe-container">
          <iframe width="466" height="400" :src='"https://www.youtube.com/embed/"+video.id.videoId'></iframe>
    </div>    
  </b-modal>
  <b-button v-b-modal="'myModal'+video.id.videoId" class="boton">¡VER VIDEO!</b-button>
      </div>
  </div>
  </div>
</div>

</div>
</div>
   


</template>
<script>
import Isotope from 'isotope-layout'
import Youtubenav from '../components/Youtubenav'
import axios from "axios"
export default {
  data() {
    return {
      videos:null,
      search:'',
      isotope:null
    }
  },
    components:{
        Youtubenav
    },
    name: 'Youtube',
    methods:{
        async getVideos(){
          let params ={
            part :'snippet',
            channelId:"UCbx_d228PdYwgB4Jz202SIQ",
            key: 'AIzaSyCyL3VYk6Fbkwuo7JoBmPGVVMdYJTawqOY',
            q: this.search,
            maxResults:2,
            type: 'video'

          }
            let datos = await axios.get('https://youtube.googleapis.com/youtube/v3/search',{params})
            this.videos = datos.data.items
          
        },
         searchData(){
        this.getVideos()      
    },
    relayoutTheGrid(){
      setTimeout(()=>{
        let elem = document.querySelector('.grid');
      this.isotope = new Isotope(elem, {
        itemSelector: '.card',
        layoutMode: 'masonry'
      });
      },1)
      
    }     
    },

    created(){
        this.getVideos()
        this.relayoutTheGrid();
     
    }
}

</script>

<style> 
body{
  background-color: #040F20 ;
}

img{
  align-items: center;
}
.input-text{
  border-radius: 0.8rem;
  width: 100%;
  padding: 0.6rem;
  outline: none;
  border: none;
  box-shadow: 0px 1px 8px #EA1889 ;
  transition: 0.4s all ease-out;
  transform: translateY(2.3rem);
}
.input-text:hover{
  box-shadow: 0px 9px 32px -1px #EA1889;

}
#input-titulo{
  text-align: center;
}
::placeholder{
  color: #A8A8A8;
  font-family: 'Lato', sans-serif;
  font-size: 1rem;
}

.card{
  box-shadow: 0px 9px 32px -1px #EA1889;
  transition: all 0.3s ease-in;
  opacity: 0.5;
}

.card:hover{
  transform: scale(1.1);
  opacity: 1;
  box-shadow: 0px 9px 32px -1px #FB0A8B
;
}
.card-text h6{

  font-size: 0.7rem;
  font-family: 'Poppins', sans-serif;
  font-weight: 700;

}

.card-text p{
  font-size: 0.6rem;
  font-family:'Lato', sans-serif;
  font-weight: 400;
}

.boton{
  width: 100%;
  background-color: #EA1889  !important;
  border:none;
  transition: all 0.3s ease-in-out;
  outline: none;
  font-family:'Poppins', sans-serif ;
  font-weight: 500;

}
.boton:hover{
  color: #FFA5D5;
}
.modal-footer{
  display: none;
}

.iframe-container{
  position: relative;
  padding-bottom: 56.25%;
  padding-top: 35px;
  height: 0;
  overflow: hidden;
}
.iframe-container iframe{
    position: absolute;
    top:0;
    left: 0;
    width: 100%;
    height: 100%;
}

/* Media Queries */
@media screen and (max-width:980px){

.input-container{
  display: flex;
  justify-content: center;
}
.input-text{
  width: 80%;
  
}
}

@media screen and (max-width:1024px){
  .card-body h6{
    font-size: 1rem;
  }
  .card-body p{
    font-size: 0.7rem;
  }
.card .mx-auto{
  margin-top: 1rem;
}

}


</style>