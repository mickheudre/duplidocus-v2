<template>
  <div>
    <span>{{ date }}</span>
    <nuxt-link :to="`evenements/${id}`">
      <h6 class="subtitle is-6 has-text-weight-semibold">
        {{ name }}
      </h6>
    </nuxt-link>
    <span class="is-italic">
      {{ description }}
    </span>
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
