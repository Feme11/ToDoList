<template>
  <div>
    <h1>Agrega una tarea a tu lista</h1>

    <input type="text" v-model="tarea">
    <button @click="add">Agregar tarea</button>

    <ul>
      <li v-for="tarea in lista_tareas" :key="tarea">{{tarea}}</li>
    </ul>
  </div>
</template>
<script>
export default {
  data() {
    return {
      tarea: " ",
      lista_tareas: []
    };
  },
  methods: {
    add(){
      this.lista_tareas.push(this.tarea),
      this.tarea = ''
    }
  },
};
</script>