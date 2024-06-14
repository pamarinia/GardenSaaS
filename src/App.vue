<template>
  <main>
    <div v-if="showModal" class="overlay">
      <div class="modal">
        <textarea name="note" id="note" cols="30" rows="10"></textarea>
        <button>Add note</button>
        <button class="close" @click="showModal = false">Close</button>
      </div>
    </div>
    
    <div class ="container">
      <header>
        <h1>Notes</h1>
        <button @click="showModal = true">+</button>
      </header>

      <div class="cards-container">
        <div class="card">
          <p class="main-text">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ratione ex aut voluptate, maxime distinctio numquam.</p>
          <p class="date">04/27/2019</p>
        </div>
        <div class="card">
          <p class="main-text">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ratione ex aut voluptate, maxime distinctio numquam.</p>
          <p class="date">04/27/2019</p>
        </div>
      </div>
    </div>
  </main>
</template>


<script setup lang="ts">
  import { ref } from 'vue';

  const showModal = ref(false);
</script>


<style scoped>
main {
  height: 100vh;
  width: 100vw;
}

.container {
  max-width: 1000px;
  padding: 10px;
  margin: 0 auto;
}

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

h1 {
  font-weight: bold;
  margin-bottom: 25px;
  font-size: 75px;
}

header button {
  border: none;
  padding: 10px;
  width: 50px;
  height: 50px;
  cursor: pointer;
  background-color: #202020;
  border-radius: 100%;
  color: white;
  font-size: 20px;
}

.cards-container {
  display: flex;
  flex-wrap: wrap;
}

.card {
  width: 225px;
  height: 225px;
  background-color: rgb(255, 255, 122);
  padding: 10px;
  border-radius: 15px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  margin-right: 20px;
  margin-bottom: 20px;
}

.date {
  font-size: 12px;
  font-weight: bold;
}

.overlay {
  position: absolute;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  display: flex;
  align-items: center;
  justify-content: center;
}

.modal {
  width: 750px;
  background-color: white;
  border-radius: 10px;
  padding: 30px;
  position: relative;
  display: flex;
  flex-direction: column;
}

.modal button {
  padding: 10px 20px;
  font-size: 20px;
  width: 100%;
  background-color: blueviolet;
  border: none;
  color: white;
  cursor: pointer;
  margin-top: 10px;
}

.modal .close {
  background-color: red;
}
</style>
