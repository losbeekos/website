<template>
  <div class="form-row">
    <slot />
  </div>
</template>

<style scoped>
.form-row {
  margin-bottom: var(--size-32);
}

.form-row:first-of-type {
  margin-top: var(--size-40);
}
</style>