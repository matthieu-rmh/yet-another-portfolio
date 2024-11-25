<script setup lang="ts">
defineProps<{
  msg: string
}>()
</script>

<template>
  <div id="main__banner__container">
    <div class="main__banner__inner__container">
        <h1 id="leftside__bigtext__banner">{{ msg }}</h1>
        <div id="ticking__cursor"></div>
    </div>
    <div id="main__banner__img__circle__container" class="main__banner__inner__container">
        <div id="img__circle__container"></div>
    </div>
  </div>
</template>

<style scoped>

#img__circle__container{
    display: block;
    height: 20rem;
    width: 20rem !important;
    margin: auto;
    border-radius: 20rem;
    border: 5px solid white;
}

#main__banner__img__circle__container{
    display: block !important;
    align-content: center !important;
}

#ticking__cursor{
    width: 0.5rem !important;
    height: 5rem;
    background-color: #3e8fb0;

}

.main__banner__inner__container{
    padding: 4rem;
    display: block ruby;
    align-content: center;
}

#main__banner__container{
    display: flex;
    width: 100%;
    height: 35rem;
}

#main__banner__container div{
    width: 50%;
}

h1 {

    font-weight: 500;
    font-size: 2.6rem;
    position: relative;
    top: -10px;
    color: #3e8fb0;
    /*margin: 10px 0 0 10px;*/
    overflow: hidden;
    white-space: nowrap;
    /*width: 100%;*/
    /* we set steps to 31 as we have a text of 31 charachters including 
     white-space*/
}

#leftside__bigtext__banner{
    /*width: 100%;*/
    width: 24ch;
    /*width: fit-content;*/
    animation: type 1.5s steps(24, end);
}

#main__banner__container h1,{
  text-align: center;
}

@media (min-width: 1024px) {
  #main__banner__container h1{
    text-align: left;
  }
}
@keyframes type{ 
  from { width: 0ch; } 
  /*to { width: 24ch; } */
}

</style>
