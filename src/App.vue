<template>
  <div>
    <h1>Crea tu lista!</h1>
    <input type="text" v-model="value" placeholder="Valor a añadir en la lista" />

    <ul class="list">
      <li class="listElement" v-for="value in valuesArray" :key="value">{{value}}</li>
    </ul>
    <button @click="setValue(value)">Agregar a la lista</button>
  </div>
</template>

<script>
export default {
  name: "app",
  data: () => {
    return {
      valuesArray: [],
      value: ""
    };
  },
  methods: {
    setValue: function(value) {
      this.valuesArray.push(value);
      this.value = "";
    }
  }
};
</script>