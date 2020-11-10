<template>
  <div class="is-centered">
    <GuideChapter file="intro.md" />
    <GuideChapter id="riso" file="part1.md" class="row-reverse" />
    <GuideChapter id="defauts" file="part2.md" />
    <GuideChapter id="format" file="part3.md" class="row-reverse" />
    <GuideChapter id="préparation" file="part4.md" />
    <GuideChapter id="prix" file="part5.md" class="row-reverse" />
  </div>
</template>

<script>
import GuideChapter from '~/components/GuideChapter'

export default {
  components: {
    GuideChapter
  }
}
</script>

<style lang="scss" scoped>

.columns {
  flex: 1;
  margin: 0;
  justify-content: center;
  align-items: center;
  margin: 8em 0;
}

.row {
  flex-direction: row;
}
.row-reverse {
  flex-direction: row-reverse;
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
