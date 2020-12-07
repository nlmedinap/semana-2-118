<template>
  <div id="app">
<div class="container-fluid">
  <section-api></section-api>
  </div> 


    <div class="container-fluid">
      <div class="row justify-content-center mb-5">
        <div class="col mt-5" v-for="(item, index) of team" :key="index">
          >
          <team-card v-bind:member="item"></team-card>
        </div>
      </div>
    </div>

    <page-footer></page-footer>
    <h1>{{ title }}</h1>
  </div>
</template>
npm run serv
<script>
import PageFooter from "./components/PageFooter.vue";
import TeamCard from "./components/TeamCard.vue";
import SectionApi from "./components/SectionApi.vue";

export default {
  name: "App",
  components: {
    PageFooter,
    TeamCard,
    SectionApi
  },
  data() {
    return {
      title: "",

      team: [
        {
          codigo: 1,
          nombre: "Carlos Valencia",
          descripcion:
            "Encargado de la parte visual e interactiva de la página Web",
          rol: "Desarrollador FrontEnd",
          image: "../img/Carlos.png",
        },
        {
          codigo: 2,
          nombre: "Luz Orjuela",
          descripcion:
            "Lider de equipo y administrador del proyecto, además, encargado de averiguar las actividades y garantizar que se realicen.",
          rol: "Lider de equipo y dueña de producto",
          image: "../img/Luz.png",
        },
        {
          codigo: 3,
          nombre: "Pablo Pelaez",
          descripcion:
            "Se encarga de trabajar la arquitectura interna de la página Web que se encuentra vinculado a todo el contenido que el usuario ve al final",
          rol: "Desarrollador BackEnd",
          image: "../img/JP.jpeg",
        },
        {
          codigo: 4,
          nombre: "Lucia Medina",
          descripcion:
            "Encargado de la parte visual e interactiva de la página Web",
          rol: "Desarrollador FrontEnd",
          image: "../img/Lucia.png",
        },
      ],
    };
  },
};
</script>

