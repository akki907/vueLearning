<template>
  
    <div class="col-lg-12">
       <nav class="navbar navbar-light ">
        <span class="navbar-text">
         Navbar
        </span>
        </nav>
    </div>

</template>

<script>
export default {
  name: "Navbar",
  props: {
    msg: String
  },
  data() {
    return {
      name: "test"
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
