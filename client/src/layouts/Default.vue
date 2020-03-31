<template>
  <div class="layout">
    <div class="container">
      <NavBar/>
      <slot/>
      <FootBar/>
    </div>
  </div>
</template>

<style lang="scss">
@import url('https://fonts.googleapis.com/css?family=Poppins&display=swap');
.layout {
  height: 100%;
}
</style>
