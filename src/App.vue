<template>
  <div class="container">
    <div class="row">
      <div class="col-md-6 col-md-offset-3">
        <br>
        <button @click="selectedComponent = 'appMemory'" class="btn btn-primary">Memory Componenti</button>
        <button @click="selectedComponent = 'appNewMemory'" class="btn btn-primary">NewMemory Componenti</button>
        <button @click="selectedComponent = 'appAuthor'" class="btn btn-primary">Author Componenti</button>
        <hr>
        <component :is="selectedComponent">
          <h3 slot="heading">Başlık</h3>
          <p>Bu çok güzel bir anıydı...</p>
        </component>
        <!-- <app-memory>
          <h3 slot="heading">Başlık</h3>
          <p>Bu çok güzel bir anıydı...</p>
        </app-memory> -->
      </div>
    </div>
  </div>
</template>

<script>
  import Memory from "./Components/Memory";
  import NewMemory from "./Components/NewMemory"
  import Author from "./Components/Author"
export default {
  data() {
    return {
      selectedComponent: "appMemory"
    }
  },
    components : {
      appMemory : Memory,
      appNewMemory : NewMemory,
      appAuthor : Author
    }
  }
</script>
