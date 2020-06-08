<template>
  <div>
      <h5 class="title">
        Evénements
      </h5>
    <div class="event-category">
    <Event v-for="event in nextEvents" :key="event.id" v-bind="{id: event.id, ...event.data}" />
    </div>
    <div class="event-category">
    <h5 class="title is-5">
      Événements passés
    </h5>
    <Event v-for="event in pastEvents" :key="event.id" class="event" v-bind="{id: event.id, ...event.data}" />
    </div>
  </div>
</template>

<script>
import Event from '~/components/event'
const moment = require('moment')

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
  computed: {
    pastEvents () {
      return this.events.filter(event => (moment() > moment(event.id.substring(1, 12))))
    },
    nextEvents () {
      return this.events.filter(event => (moment() <= moment(event.id.substring(1, 12))))
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

<style lang="scss" scoped>

.title.is-5:not(:last-child) {
  margin: 2.5em 0 1em 0;
}

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

.image-color {
  background-color: #00838A;
  mix-blend-mode: multiply;
  display: inline-block;

}
.image {
  mix-blend-mode: screen;
  max-height: 400px;
}

.event {
margin: 1em 0;
}

</style>
