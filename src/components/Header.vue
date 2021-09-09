<template>
  <header>
    <nav class="navbar navbar-light my-bg-nav">
      <div class="container-fluid">
        <a class="navbar-brand" href="#">
          <img src="../assets/img/logo.png" alt="" height="35" />
        </a>
        <div class="d-flex">
          <select class="form-select" aria-label="Default select example">
            <option selected>Open this select menu</option>
            <option value="1">One</option>
            <option value="2">Two</option>
            <option value="3">Three</option>
          </select>
          <button class="btn btn-outline-success" type="submit">Reset</button>
        </div>
      </div>
    </nav>
  </header>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style lang="scss">
.logo {
  height: 40px;
}
.my-bg-nav {
  background-color: #2e3a46;
}
</style>