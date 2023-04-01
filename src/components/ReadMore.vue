<!-- 2. Configura el componente 'ReadMore' para que se pueda mostrar el texto completo cuando el usuario hace click en el botón 'Show more'. Cuando el texto este desplegado el botón tiene que mostrar 'Show less'. El parágrafo está utilizando la class 'cut-text' disponible en el archivo src/asserts/readmore.css. -->

<script setup>
import { ref } from "vue";

const title = ref("Exercise Read More");
const isActive = ref(false);

  const showAll = () => {
    isActive.value = !isActive.value;
  };


</script>

<template>
  <div class="container text-center">
    <h1 class="my-3">{{ title }}</h1>
    <div>
      <p class="mb-3 d-block" :class="{'cut-text': !isActive}">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dignissimos
        ipsa neque odio consectetur impedit tempore modi accusantium! Voluptatem
        molestiae nemo inventore soluta corrupti. Culpa perferendis sapiente
        deserunt aperiam maxime consectetur recusandae quasi commodi dicta
        temporibus pariatur ab repellendus dignissimos natus aliquam odit ullam,
        quaerat autem non hic, quidem dolore laboriosam.
      </p>
      <button @click="showAll"   class="btn btn-primary">{{ isActive ? "Show Less" : "Show More" }}</button>
    </div>
    <hr class="mb-4" />
  </div>
</template>

<style lang="css"></style>
