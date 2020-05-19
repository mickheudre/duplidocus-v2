<template>
  <div id="app-container" class="container">
    <nav class="navbar" role="navigation" aria-label="main navigation">
      <div class="navbar-brand">
        <a class="navbar-item" href="">
          <h4 class="title is-4">Duplidocus</h4>
        </a>
      </div>

      <div class="navbar-menu">
        <div class="navbar-end">
          <a class="navbar-item">
            <h6 class="subtitle is-6">Guide d'impression?</h6>
          </a>
          <a class="navbar-item">
            <h6 class="subtitle is-6">Evènements</h6>
          </a>
          <a class="navbar-item">
            <h6 class="subtitle is-6">Liens</h6>
          </a>
        </div>
      </div>
    </nav>
    <div id="pages" class="containers">
      <nuxt />
    </div>
  </div>
</template>

<style lang="scss">
#app-container {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
}
#pages {
  flex: 1;
  display: flex;
}
.navbar {
  margin: 0 2em 0 2em;
  padding: 8px;
}

.content-item {
  flex: 1
}

a.navbar-item:hover {
    background-color: transparent;
    text-decoration: underline;
}
</style>
