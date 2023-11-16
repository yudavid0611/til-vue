<script setup>
import DeclarativeRenderig from './components/DeclarativeRenderig.vue'
import AttributeBindings from './components/AttributeBindings.vue'
import EventListener from './components/EventListener.vue'
import FormBindings from './components/FormBindings.vue'
import ConditionalRendering from './components/ConditionalRendering.vue'
import ListRendering from './components/ListRendering.vue'
</script>

<template>
    <div>
        <h1>1. 선언적 렌더링</h1>
        <DeclarativeRenderig></DeclarativeRenderig>
        
        <br>

        <h1>2. 속성 바인딩</h1>
        <AttributeBindings></AttributeBindings>

        <br>

        <h1>3. 이벤트 리스너</h1>
        <EventListener></EventListener>

        <br>

        <h1>4. 폼 바인딩(양방향 바인딩)</h1>
        <FormBindings></FormBindings>
        
        <br>

        <h1>5. 조건부 렌더링</h1>
        <ConditionalRendering></ConditionalRendering>

        <br>

        <h1>6. 리스트 렌더링</h1>
        <ListRendering></ListRendering>
        
        
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
