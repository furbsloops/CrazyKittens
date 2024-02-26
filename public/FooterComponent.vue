<template>
  <footer :style="{ backgroundColor: backgroundColor }">
    <h1>Crazy Kittens</h1>
  </footer>
</template>

<script>
export default {
  name: "FooterComponent",
  data() {
    return {
      backgroundColor: this.getRandomColor(),
    };
  },
  methods: {
    getRandomColor() {
      // Funzione per generare un colore casuale in formato hex
      const letters = "0123456789ABCDEF";
      let color = "#";
      for (let i = 0; i < 6; i++) {
        color += letters[Math.floor(Math.random() * 16)];
      }
      return color;
    },
  },
};
</script>

<style scoped>
footer {
  padding: 20px;
  color: white;
  text-align: center;
}
h1 {
  margin: 0;
}
</style>
