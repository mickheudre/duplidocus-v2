<template>
  <div>
    <h6>{{ date }}</h6>
    <nuxt-link :to="`evenements/${id}`">
      <h6 class="has-text-weight-semibold">
        {{ name }}
      </h6>
    </nuxt-link>
    <h7 class="is-size-7">
      {{ description }}
    </h7>
    <br>
    <br>
  </div>
</template>

<script>
export default {
  name: 'Event',
  props: {
    id: String,
    date: String,
    name: String,
    description: String
  }
}
</script>
