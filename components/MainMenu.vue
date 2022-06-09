<template>
  <div class="side-bar">
    <div class="logo"><Logo/></div>
    <div class="said-main">
      <ul class="main">
        <li  class="visible" id="cero">
           <NuxtLink to="/apariencia">Actualidad al instante </NuxtLink>
        </li>
        <li @click="openMenu1 = !openMenu1" class="visible" id="open" >La Marca
          <ul class="panel" v-show="openMenu1">
            <li class="invisibl" > <NuxtLink to="/novedades">Novedades </NuxtLink></li>
            <li class="invisibl" ><NuxtLink to="/construccion">Construcción y relaciones</NuxtLink></li>
            <li class="invisibl"><NuxtLink to="/tipografia">Tipografía</NuxtLink></li>
             <li class="invisibl"><NuxtLink to="/colores">Colores</NuxtLink></li>
            <li class="invisibl"><NuxtLink to="/logo">Logo</NuxtLink></li>
              <li class="invisibl"><NuxtLink to="/layout">Layout</NuxtLink></li>
              <li class="invisibl"><NuxtLink to="/imagenes">Imágenes</NuxtLink></li>
              <li class="invisibl"><NuxtLink to="/infografia">Infografía</NuxtLink></li>
          </ul>
        </li>
        <li @click="openMenu2 = !openMenu2" class="visible">BÁSICOS
          <ul class="panel" v-show="openMenu2">
            <li class="invisibl" > <NuxtLink to="/rotulaciones">Rotulaciones</NuxtLink></li>
            <li class="invisibl" > <NuxtLink to="/animaciones">Animaciones</NuxtLink></li>
          </ul>
        </li>
            <li  class="visible" id="cero">
           <NuxtLink to="/recopilatorio">Recopilatorio </NuxtLink>
        </li>
      </ul>
    </div>


  </div>
</template>
<script>
    export default {

    data(){
        return{
            openMenu1: false,
            openMenu2: false,
            openMenu3: false
           
        }
    }
    }
</script>

<style lang="postcss">
.side-bar{
    scroll-behavior: smooth;
     background-color: $blanco;
    width: 40vh;
    height: 100vh;
    position: fixed;
    box-shadow: $sombra1;
}
ul{
     font-size: 12pt;
      font-style: 400;
      color: $azul;
}
li{
     font-size: 12pt;
        font-style: 400;
        color: $azul;
        @apply ml-11 mt-8;
          
}
  #cero{
    margin-top: 0;
  }
    
</style>
