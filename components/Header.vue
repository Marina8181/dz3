<template>
  <header>
    <h1>Добро пожаловать!</h1>
  </header>
</template>

<style scoped lang="scss">
@use "@/assets/scss/variables" as vars;

header {
  background-color: lightblue;
  padding: 20px;
  margin: 10px;
  text-align: center;

  h1 {
    font-family: var(--font-family-two), sans-serif;
  }
}
</style>