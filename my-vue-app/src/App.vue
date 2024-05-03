<template>
  <div class="container">
    <h1 style="font-weight: bold;">Ririn Juliyanti</h1>
    <p>Selamat Datang di Matakuliah Praktikum Pemrograman Berbasis Komponen </p>
    
    <!--  Elemen input teks -->
    <input type="text" v-model="inputText" placeholder="Masukkan Teks">
    
    <!--  class bindings dan style bindings -->
    <div class="content" :class="{ 'highlight': isHighlighted }" :style="{ 'font-weight': isBold ? 'bold' : 'normal' }">
      Saya adalah mahasiswi Teknik informatika Angkatan 2022.
    </div>
    
    <!--  event listeners -->
    <button @click="toggleHighlight">Toggle Highlight</button>
    <button @click="toggleBold">Toggle Bold</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      inputText: '',
      isHighlighted: false,
      isBold: false
    };
  },
  methods: {
    toggleHighlight() {
      this.isHighlighted = !this.isHighlighted;
    },
    toggleBold() {
      this.isBold = !this.isBold;
    }
  }
};
</script>

<style>
.container {
  border: 2px solid rgb(64, 38, 211);
  padding: 20px;
  box-shadow: 10px 10px 5px rgba(47, 12, 247, 0.2);
}
.highlight {
  background-color: skyblue;
}
</style>
