<script setup>
import Header from '@/components/Header.vue'
import Banner from '@/components/Banner.vue'
import Card from '@/components/Card.vue'
import Footer from '@/components/Footer.vue'
</script>

<template>
  <div>
    <Header />
    <Banner />

    <div class="container">
      <Card title="Кто я?">
        <img src="/pictures/пингвин.jpg" alt="пингвин" class="card-image">
        <ul>
          <li>Студентка ДВФУ</li>
          <li>Любитель кошек</li>
          <li>Кофеман</li>
        </ul>
      </Card>

      <Card title="Здравствуйте" is-middle>
        <img src="/pictures/китик.png" alt="котенок" class="card-image">
      </Card>

      <Card title="Что это за сайт?">
        <img src="/pictures/сова.jpg" alt="сова" class="card-image">
        <p>Это третья домашняя работа по frontend разработке.</p>
      </Card>
    </div>

    <Footer />
  </div>
</template>

<style scoped lang="scss">
:root {
  --font-family-one: 'Open Sans', sans-serif;
  --font-family-two: 'Montserrat', sans-serif;
  font-family: var(--font-family-two), sans-serif;
}

.container {
  display: flex;
  gap: 10px;
}

.card-image {
  width: 100%;
  height: auto;
  border-radius: 10px;
  margin-bottom: 15px;
}
</style>