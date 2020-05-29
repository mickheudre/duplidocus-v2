<template>
  <div class="columns is-centered">
    <div class="column is-1" />
    <div class="column">
      <div class="images">
        <div class="align-right">
          <div class="image-color">
            <img class="image" src="../assets/group.png">
          </div>
        </div>
      </div>
    </div>
    <div class="column is-1" />
    <div class="column is-4">
      <h5 class="title">
        {{ title }}
      </h5>
      <links />
    </div>
    <div class="column is-1" />
  </div>
</template>

<script>
import linkData from '~/content/links.md'

export default {
  components: {
    links: linkData.vue.component
  },
  computed: {
    title () {
      return linkData.attributes.title
    }
  }
}
</script>

<style lang="scss" scoped>
.columns {
  flex: 1;
  margin: 0;
  justify-content: center;
  align-items: center;
  flex-direction: row-reverse;
}
.columns:last-child {
  margin-bottom: 0;
}

p {
  line-height: 1.5em;
}

.images {
  display: flex;
  flex-direction: column;
  flex: 1;
}

.title:not(:last-child){
  margin: .4em 0;
}

.image-color {
  background-color: #00838A;
  mix-blend-mode: multiply;
  display: inline-block;

}
.image {
  mix-blend-mode: screen;
}
h6:not(:last-child) {
  margin: 1.5rem 0 .4rem 0;
}

</style>
