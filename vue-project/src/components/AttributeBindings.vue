<template>
    <div>
        <!-- 속성을 동적 값에 바인딩 -->
        <!-- <h2 v-bind:class="titleClass">Make me red!</h2> -->
        <h2 :class="titleClass">Make me red!</h2>
    </div>
</template>

<script>
export default {
    data() {
        return {
            titleClass: 'title'
        }
    }
}
</script>

<style>
.title {
    color: red;
}
</style>