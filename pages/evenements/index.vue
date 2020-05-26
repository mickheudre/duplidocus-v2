<template>
  <div>
    <h5 class="title">
      Événements passés
    </h5>
    <Event v-for="event in events" :key="event.id" v-bind="{id: event.id, ...event.data}" />
  </div>
</template>

<script>
import Event from '~/components/event'

export default {
  name: 'Liens',
  components: {
    Event
  },
  data () {
    return {
      events: []
    }
  },
  mounted () {
    this.importAll(require.context('~/content/events', true, /\.md$/))
  },
  methods: {
    importAll (r) {
      r.keys().forEach(key => (this.events.push({ id: key.replace(/\.[^/.]+$/, ''), data: r(key).attributes })))
    }
  }
}
</script>

<style lang="scss">

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

.divider {
  width: 150px;
  margin: 0
}

.divider:last-of-type {
  margin-bottom: 2em;
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
  max-height: 400px;
}

</style>
