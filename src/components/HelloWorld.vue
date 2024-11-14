<script setup lang="ts">
defineProps<{
  msg: string
}>()
</script>

<template>
  <div class="greetings">
    <h1 class="green">{{ msg }}</h1>
    <!-- <h3>
      You’ve successfully created a project with
      <a href="https://vite.dev/" target="_blank" rel="noopener">Vite</a> +
      <a href="https://vuejs.org/" target="_blank" rel="noopener">Vue 3</a>.
    </h3>
    -->
  </div>
</template>

<style scoped>
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
    animation: type 1.3s steps(31, end);
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
@keyframes type{ 
  from { width: 0; } 
}

</style>
