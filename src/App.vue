<template>
  <div id="app">
    <div class="container">
      <div class="row header my-5 p-3">
        <div class="col-lg-12">
          <h2>What I do today?</h2>
        </div>
      </div>
      <div class="row">
        <div class="col-lg-12">
          <div class="pekerjaan-rumah">
            <div class="row">
              <div
                v-for="tugasSaya in tugas"
                :key="tugasSaya.id"
                class="col-lg-12 mb-3 text-left tugas"
              >
                <div class="form-check">
                  <ItemTugas :tugasSaya="tugasSaya" />
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import "bootstrap/dist/css/bootstrap.css";

import ItemTugas from "./components/ItemTugas.vue";

export default {
  name: "app",
  data: function() {
    return {
      tugas: [
        {
          id: 1,
          deskripsi: "Melanjutkan tugas projek UAS",
          isDone: false,
        },
        {
          id: 2,
          deskripsi: "Mengerjakan projek website laravel dan vue js",
          isDone: false,
        },
        {
          id: 3,
          deskripsi: "Menonton film dan anime",
          isDone: false,
        },
        {
          id: 4,
          deskripsi: "Makan 3 kali sehari",
          isDone: false,
        },
      ],
    };
  },
  components: {
    ItemTugas,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}

.header {
  background: #1abc9c;
}

.header h2 {
  margin: 0;
}

.tugas .item {
  font-size: 18px;
}

.item-completed {
  color: #1abc9c;
}
</style>
