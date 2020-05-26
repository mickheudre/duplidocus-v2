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
      <hr class="divider">
      <h4 class="title">
        Duplidocus est <br>
        un collectif <br>
        d’impressions <br>
        DIY & libertaires
      </h4>
      <hr class="divider">
      <p class="is-size-6">
        Nous imprimons affiches, brochures, fanzines,<br>
        tracts, petits ouvrages en risographie. <br>
        Nous ne sommes pas des professionnel.le.s,<br>
        les tirages sont des moments de rencontres,<br>
        d’échanges et de complicité.
      </p>
    </div>
    <div class="column is-1" />
  </div>
</template>

<script>
// export default {

// }
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
}

</style>
