<template>
    <div>
        <button @click="toggle">토글 버튼</button>
        <!-- v-if 디렉티브를 사용하여 엘리먼트를 조건부로 렌더링한다. -->
        <h2 v-if="awesome">Vue는 굉장해!</h2>
        <h2 v-else>Vue는 별로야...</h2>
    </div>
</template>
<script>
export default {
    data() {
        return {
            awesome: true
        }
    },
    methods: {
        toggle(e) {
            this.awesome = !this.awesome
        }
    }
}
</script>
<style>
    
</style>