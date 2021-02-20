<template>
  <div id="app">
    <Header />
    <div class="main">
      <div class="container">
        <div class="row">
          <div class="col-12"><Shop /></div><hr>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Header from "./components/Header";
import Shop from "./components/Shop";


export default {
  name: "App",
  components: {
    Shop,
    Header,
    
  },
};
</script>

<style>
*{
  margin: 0px;
  padding: 0px;
  justify-content: center;
}
</style>
