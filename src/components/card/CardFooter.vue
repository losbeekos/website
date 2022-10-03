<template>
  <footer class="card-footer">
    <slot />
  </footer>
</template>

<style scoped>
.card-footer {
  display: flex;
  flex-wrap: wrap;
  gap: var(--size-12) var(--size-40);
}
</style>