<script setup lang="ts">
defineProps<{
  msg: string
}>()
</script>

<template>
  <div id="main__banner__container">
    <div style="background-color: lightgreen;">
        <h1 id="leftside__bigtext__banner">{{ msg }}</h1>
    </div>
    <div style="background-color: lightpink;">
        <h1>right</h1>
    </div>
  </div>
</template>

<style scoped>

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
    width: 100%;
    /* we set steps to 31 as we have a text of 31 charachters including 
     white-space*/
}

#leftside__bigtext__banner{
    animation: type 1.3s steps(31, end);
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
  from { width: 0; } 
}

</style>
