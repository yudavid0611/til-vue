<script setup>
import DeclarativeRenderig from './components/DeclarativeRenderig.vue'
import AttributeBindings from './components/AttributeBindings.vue'
</script>

<template>
    <div>
        <h1>1. 선언적 렌더링</h1>
        <DeclarativeRenderig></DeclarativeRenderig>
        
        <br>

        <h1>2. 속성 바인딩</h1>
        <AttributeBindings></AttributeBindings>

        <br>
        
    </div>

</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
