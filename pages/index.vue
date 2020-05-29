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
    <div class="column is-2" />
    <div class="column is-3">
      <hr class="divider">
      <h4 class="title">
        Duplidocus est <br>
        un collectif <br>
        d’impressions <br>
        DIY & libertaires
      </h4>
      <hr class="divider">
      <p>
        Nous imprimons affiches, brochures, fanzines, tracts et petits ouvrages en risographie.
      </p>
      <p>
        Nous ne sommes pas des professionnel.le.s, les tirages sont des moments de rencontres, d’échanges et de complicité.
      </p>
    </div>
    <div class="column is-1" />
  </div>
</template>

<script>
// export default {

// }
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

.divider {
  width: 150px;
  margin: 0
}

.divider:last-of-type {
  margin-bottom: 2em;
}

p {
  line-height: 1.5em;
  margin-bottom: 8px;
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
