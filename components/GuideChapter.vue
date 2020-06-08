<template>
  <div class="columns is-centered">
    <div class="column is-1" />
    <div class="column is-5">
    <!-- <Guide /> -->
      <component :is="document.vue.component" />
    </div>
    <div class="column is-1" />
    <div class="column is-4">
      <div class="image-color">
        <img class="image" :src="image">
      </div>
    </div>
    <div class="column is-1" />
  </div>
</template>

<script>

export default {
//   components: {
//     Guide: this.document.vue.component
//   },
  props: {
    file: {
      type: String,
      default: 'intro.md'
    }
  },
  computed: {
    document () {
      return require('~/content/guide/' + this.file)
    },
    image () {
      return require('~/assets/' + this.document.attributes.image)
    }
  }

}
</script>

<style lang="scss">

ol {
  margin: 16px;
}

li > a {
  font-style: italic;
}

p {
  margin-bottom: 16px;
}

.row {
  flex-direction: row;
}

.row-reverse {
  flex-direction: row-reverse;
}

.image-color {
  background-color: #00838A;
  mix-blend-mode: multiply;
  display: inline-block;

}
.image {
  mix-blend-mode: screen;
  max-height: 400px;
}
</style>
