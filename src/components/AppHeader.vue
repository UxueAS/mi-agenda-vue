<template>
  <nav class="navbar bg-body-tertiary">
    <div class="container-fluid">
      <a class="navbar-brand" href="#">
        <img src="/docs/5.3/assets/brand/bootstrap-logo.svg" alt="Logo" width="30" height="24"
          class="d-inline-block align-text-top">
        <h1> AGENDA VUE </h1>
      </a>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'AppHeader'
}
</script>

<style scoped>
.container-fluid {
  background-color: #a4b8aba0;
  padding: 20px;
  text-align: center;
  box-shadow: 4px 4px 8px rgba(0, 0, 0, 0.379);
}

 h1 {
  font-family: 'courier', 'Georgia', serif;
  color: #495f50;
  font-size: 2.5em;
  font-weight: bolder;
 
}
</style>