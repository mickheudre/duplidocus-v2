<template>
  <div class="columns is-centered">
    <div class="column is-1" />
    <div class="column is-4">
      <NuxtChild :key="$route.params" />
    </div>
    <div class="column is-1" />
    <div class="column">
      <div class="images">
        <div class="align-right">
          <div class="image-color">
            <img class="image" src="~/assets/dupli.png">
          </div>
        </div>
      </div>
    </div>
    <div class="column is-1" />
  </div>
</template>

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
