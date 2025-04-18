<template>
  <ClientOnly>
    <div class="banner">
      <p id="greeting" class="greeting-text">{{ greetingText }}</p>
      <button
          class="greeting-button"
          @click="handleGreetingChange"
      >
        Поменять приветствие
      </button>
    </div>
  </ClientOnly>
</template>

<script setup>
const greetingText = ref("Hello, World");

const handleGreetingChange = () => {
  greetingText.value = greetingText.value === "Hello, World"
      ? "Hello, FEFU"
      : "Hello, World";
};

// Для SSR-совместимости
onMounted(() => {
  // Любая клиент-специфичная логика
});
</script>

<style scoped lang="scss">
@use "@/assets/scss/mixins" as mixins;
@use "@/assets/scss/variables" as vars;

.banner {
  @include mixins.card-styles;
  background-color: var(--light-blue); /* Используем переменную */
  text-align: center;
  padding: 20px;
  margin: 10px;
  transition: background-color 0.3s ease;

  .greeting-text {
    margin: 0 0 12px 0;
    font-size: 1.2rem;
    color: var(--text-dark);
  }

  .greeting-button {
    margin-top: 10px;
    padding: 8px 16px;
    cursor: pointer;
    background-color: white;
    border: 1px solid var(--border-color);
    border-radius: 4px;
    transition: all 0.2s ease;

    &:hover {
      background-color: #f0f0f0;
    }
  }
}
</style>