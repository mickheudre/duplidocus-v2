<template>
  <div id="app-container" class="container">
    <nav class="navbar" :class="{'is-active': showMenu}" role="navigation" aria-label="main navigation">
      <div class="navbar-brand">
        <nuxt-link class="navbar-item" to="/">
          <h4 class="title is-4" :class="{'is-active': showMenu}">
            Duplidocus
          </h4>
        </nuxt-link>
        <a
          role="button"
          class="navbar-burger burger"
          aria-label="menu"
          aria-expanded="false"
          data-target="duplidocusNav"
          :class="{ 'is-active': showMenu }"
          @click="showMenu = !showMenu"
        >
          <span aria-hidden="true" />
          <span aria-hidden="true" />
          <span aria-hidden="true" />
        </a>
      </div>

      <div id="duplidocusNav" class="navbar-menu" :class="{ 'is-active': showMenu } ">
        <div class="navbar-end">
          <nuxt-link class="navbar-item" to="/guide">
            <h6 class="subtitle is-6" :class="{ 'is-active': showMenu }" @click="showMenu = false">
              Guide d'impression
            </h6>
          </nuxt-link>
          <nuxt-link class="navbar-item" to="/evenements">
            <h6 class="subtitle is-6" :class="{ 'is-active': showMenu }" @click="showMenu = false">
              Evènements
            </h6>
          </nuxt-link>
          <nuxt-link class="navbar-item" to="/gragenda">
            <h6 class="subtitle is-6" :class="{ 'is-active': showMenu }" @click="showMenu = false">
              Gragenda
            </h6>
          </nuxt-link>
          <nuxt-link class="navbar-item" to="/liens">
            <h6 class="subtitle is-6" :class="{ 'is-active': showMenu }" @click="showMenu = false">
              Liens
            </h6>
          </nuxt-link>
          <nuxt-link class="navbar-item  cta" to="/contact">
            <h6 class="subtitle is-6" :class="{ 'is-active': showMenu }" @click="showMenu = false">
              Nous Contacter
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

<script>
export default {
  data () {
    return {
      showMenu: false
    }
  }
}
</script>
<style lang="scss">

.navbar {
  padding-top: 1.5em;
}
#app-container {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
}
#pages {
  flex: 1;
  display: flex;
}

// .cta {
//   border-bottom: 2px solid;
// }

.content-item {
  flex: 1
}

.navbar-item {
  margin-left: 1em;
  // margin-right: 1em;
}

a.navbar-item:hover {
    background-color: transparent;
    text-decoration: underline;
    text-decoration-thickness: 2px;
}

a.navbar-item.nuxt-link-exact-active.nuxt-link-active {
    background-color: transparent;
}

.navbar-menu {
  box-shadow: none;
}

.is-active {
  background-color: #00838A;
  color: #EEEEEC
}

.navbar-menu.is-active {
  position: absolute;
  width: 100%;

}

.navbar-burger:hover {
  background-color: transparent;
}

h6:not(:last-child) {
  margin: 1.5em 0 .5em 0;
}

</style>
