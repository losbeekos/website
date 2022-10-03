<template>
  <article class="card">
    <slot />
  </article>
</template>

<style scoped>
.card {
  --card-margin: clamp(var(--size-40), calc(1rem + 4vw), var(--size-60));

  display: flex;
  flex-flow: column;
  gap: clamp(var(--size-16), calc(1rem + 4vw), var(--size-32));
  width: 100%;
  margin-top: var(--card-margin);
  margin-bottom: var(--card-margin);
  background: var(--gradient-light);
  box-shadow: 0px var(--size-4) var(--size-40) var(--size-8) rgba(0, 0, 0, 0.05);
  border-radius: clamp(var(--size-16), calc(1rem + 4vw), var(--size-32));
  padding: var(--size-48) var(--size-40);
  color: var(--color-dark);
}

@media (min-width: 32em) {
  .card {
    width: clamp(18rem, calc(1rem + 80vw), 33.5rem);
  }

  .card-container > .card:not(:nth-child(2)) {
    margin-right: auto;
  }

  .card-container > .card:nth-child(2) {
    margin-left: auto;
  }
}
</style>