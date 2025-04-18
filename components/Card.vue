<template>
  <div :class="['card', { 'middle-card': isMiddle }]">
    <h2>{{ title }}</h2>
    <slot></slot>
  </div>
</template>

<script setup>
defineProps({
  title: String,
  isMiddle: Boolean
});
</script>

<style scoped lang="scss">
@use "@/assets/scss/variables" as vars;
@use "@/assets/scss/mixins" as mixins;

.card {
  @include mixins.card-styles;
  padding: 20px;
  margin: 10px;
  width: 400px;
  background-color: #228B22;
}

  h2 {
    margin-bottom: 15px;
  }

  .middle-card {
    flex-grow: 1;
    background-color: #FFF273;

    img {
      width: 500px;
      padding-right: 110px;
    }
  }
</style>