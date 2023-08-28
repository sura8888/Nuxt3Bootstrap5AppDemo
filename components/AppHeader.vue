<template>
<nav class="navbar navbar-light bg-light">
  <div class="container-fluid">
    <NuxtLink class="navbar-brand" to="/" style="margin: 0 auto;">
        <div class="image-text">
            <img src="~/assets/img/icon.png" alt="icon" width="50" height="55" class="d-inline-block align-text-top">
            <p>{{ user.name }}</p>
        </div>
    </NuxtLink>
  </div>
</nav>
</template>
<style>
  nav {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
  }
  .image-text {
  display: flex;
  align-items: center;
}
</style>
<script setup>
 const user = ref(useLoginUser());
</script>