<template>
  <div id="app-container" class="container">
    <nav class="navbar" role="navigation" aria-label="main navigation">
      <div class="navbar-brand">
        <nuxt-link class="navbar-item" to="/">
          <h4 class="title is-4">
            Duplidocus
          </h4>
        </nuxt-link>
      </div>

      <div class="navbar-menu">
        <div class="navbar-end">
          <!-- <nuxt-link class="navbar-item" to="/guide">
            <h6 class="subtitle is-6">
              Guide d'impression
            </h6>
          </nuxt-link> -->
          <nuxt-link class="navbar-item" to="/evenements">
            <h6 class="subtitle is-6">
              Evènements
            </h6>
          </nuxt-link>
          <nuxt-link class="navbar-item" to="/liens">
            <h6 class="subtitle is-6">
              Liens
            </h6>
          </nuxt-link>
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
    text-decoration-thickness: 2px;
}

a.navbar-item.nuxt-link-exact-active.nuxt-link-active {
    background-color: transparent;
}
</style>
