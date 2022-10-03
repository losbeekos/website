<template>
  <div class="card-container">
    <slot />
  </div>
</template>

<style scoped>
.card-container {
  --card-container-padding: clamp(var(--size-40), calc(1rem + 4vw), var(--size-60));
  
  display: flex;
  flex-flow: column;
  max-width: 65rem;
  align-items: center;
  width: 100%;
  padding-left: var(--card-container-padding);
  padding-right: var(--card-container-padding);
  margin-left: auto;
  margin-right: auto;
}
</style>