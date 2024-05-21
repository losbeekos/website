<template>
  <header class="header">
    <nav class="nav">
      <a class="link" href="#over-mij">voorstellen</a>
      <a class="link" href="#contact">contact</a>
    </nav>
  </header>
</template>

<style scoped>
.header {
  --nav-gap: var(--size-12);
  --nav-box-shadow: 0 var(--size-8) var(--size-32) rgba(0, 0, 0, 0.2);

  display: flex;
  justify-content: center;
  position: absolute;
  width: 100%;
  padding: var(--nav-gap);
}

.nav {
  padding-left: var(--nav-gap);
  padding-right: var(--nav-gap);
  display: flex;
  flex-flow: wrap;
  width: 100%;
  white-space: nowrap;
  gap: 0 var(--nav-gap);
  justify-content: center;
  align-items: center;
  border-radius: var(--size-16);
  max-width: 25rem;
}

.link {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: var(--size-56);
  font-size: var(--size-18);
  color: var(--color-alpha-dark);
  text-decoration: none;
  font-weight: 600;
}

@media (min-width: 25.6em) {
  .header {
    --nav-gap: clamp(var(--size-4), calc(1rem + 2vw), var(--size-40));
  }
}

@media (max-width: 33.6875em) {
  .nav {
    background: var(--gradient-light);
    box-shadow: var(--nav-box-shadow);
    min-height: var(--size-56);
  }
}

@media (min-width: 33.75em) {
  .nav {
    flex-flow: row;
    gap: var(--size-16);
    max-width: unset;
  }

  .link {
    background: var(--gradient-light);
    box-shadow: var(--nav-box-shadow);
    border-radius: var(--size-16);
    min-width: 10rem;
    will-change: scale;
    transition: scale var(--ease-elastic-1) var(--time-3);
  }

  @media (hover) {
    .link:hover {
      scale: 1.1;
    }
  }
}
</style>
