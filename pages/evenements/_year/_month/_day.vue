
<template>
  <div>
    <h1 class="title">
      {{ event.attributes.name }}
    </h1>
    <component :is="event.vue.component" />
  </div>
</template>

<script>

export default {
  data () {
    return {
      event: null
    }
  },
  created () {
    this.event = require(`~/content/events/${this.$route.params.year}/${this.$route.params.month}/${this.$route.params.day}.md`)
  }
}
</script>

<style lang="scss">
p {
  margin: 16px 0
}
ul, li {
  margin: 8px 0;
}
</style>
