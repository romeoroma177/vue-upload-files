<template>
   <div id="app">
    <div class="container" style="width:600px">
      <div style="margin: 20px">
        <div id="app">
        <img src="./assets/psa1.png">
    </div>
        <h3>Astig Project</h3>
        <h4>Excel file Upload</h4>
      </div>
<br /><hr />
      <upload-files>Upload</upload-files>
    </div>
  </div>
  
</template>

<script>


import UploadFiles from "./components/UploadFiles";

export default {
  name: "App",
  components: {
    UploadFiles
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
