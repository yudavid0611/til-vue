<script setup>
import DeclarativeRenderig from './components/DeclarativeRenderig.vue'
import AttributeBindings from './components/AttributeBindings.vue'
import EventListener from './components/EventListener.vue'
import FormBindings from './components/FormBindings.vue'
import ConditionalRendering from './components/ConditionalRendering.vue'
import ListRendering from './components/ListRendering.vue'
import ComputedProperty from './components/ComputedProperty.vue'
import LifecycleAndTemplateRefs from './components/LifecycleAndTemplateRefs.vue'
import Watchers from './components/Watchers.vue'
import Props from './components/Props.vue'
import Emits from './components/Emits.vue'
import Slots from './components/Slots.vue'

const greeting = '부모 컴포넌트로부터 선물 전달!'
let childMsg = '자식 컴포넌트로부터 아직 선물을 받지 못했어요ㅠ'
const slotMsg = '부모로부터 템플릿 전달!'
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
        
        <br>

        <h1>7. 계산된 속성(computed)</h1>
        <ComputedProperty></ComputedProperty>
        
        <br>

        <h1>8. 생명주기와 템플릿 참조</h1>
        <LifecycleAndTemplateRefs></LifecycleAndTemplateRefs>
        
        <br>

        <h1>9. 감시자(watch)</h1>
        <Watchers></Watchers>

        <br>

        <h1>10. Props</h1>
        <!-- 자식 컴포넌트에 데이터 전달 -->
        <Props :msg="greeting"></Props>

        <br>

        <h1>11. Emits</h1>
        <!-- 자식 컴포넌트로부터 데이터를 받아 childMsg 수정 -->
        <Emits @response="(msg) => childMsg = msg"></Emits>
        <p>{{ childMsg }}</p>
        
        <br>

        <h1>12. Slots</h1>
        <!-- Slot을 사용하여 자식 컴포넌트에 템플릿 조각 전달 -->
        <Slots>
            {{ slotMsg }}
        </Slots>
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
