<template>
  <div class="speaker--bloc">
    <div v-if="speaker.photoURL" class="container--image">
      <img :src="require(`@/assets/img/speakers/${speaker.uid}.png`)" :alt="speaker.displayName">
    </div>
    <h3>{{ speaker.displayName }}</h3>
  </div>
</template>

<script>
export default {
    props: {
        speaker: {
            type: Object,
            default () {
                return {}
            }
        }
    }
}
</script>

<style lang="scss" scoped>
@import "./../assets/scss/variables";

  .speaker--bloc{
      text-align: center;
      background-color: $color-primary;
      border-radius: 2px;
      padding: 1rem;
      color: white;
      height: 100%;

      img{
          width: 75px;
          height: 75px;
          border-radius: 50%;
          border: 3px solid white;
          object-fit: cover;
      }

      h3{
        font-size: 1rem;
      }
  }
</style>
