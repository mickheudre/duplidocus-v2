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
          <!-- <nuxt-link class="navbar-item" to="/guide">
            <h6 class="subtitle is-6" @click="showMenu = !showMenu">
              Guide d'impression
            </h6>
          </nuxt-link> -->
          <nuxt-link class="navbar-item" to="/evenements">
            <h6 class="subtitle is-6" :class="{ 'is-active': showMenu }" @click="showMenu = false">
              Evènements
            </h6>
          </nuxt-link>
          <nuxt-link class="navbar-item" to="/liens">
            <h6 class="subtitle is-6" :class="{ 'is-active': showMenu }" @click="showMenu = false">
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

#app-container {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
}
#pages {
  flex: 1;
  display: flex;
}

.content-item {
  flex: 1
}

// #duplidocusNav.is-active {
//   background-color: #00838A;
// }

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
    color: white
}

.navbar-menu.is-active {
  position: absolute;
  width: 100%;

}

.navbar-burger:hover {
  background-color: transparent;
}

</style>
