<template>
  <section class="section">
    <slot />
  </section>
</template>

<style scoped>
.section {
  display: flex;
  min-height: 100vh;
  flex-flow: column;
  justify-content: center;
  padding-top: 20vh;
  padding-bottom: 20vh;
}
</style>
