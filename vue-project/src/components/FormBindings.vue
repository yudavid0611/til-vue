<template>
    <div>
        <!-- v-bind와 v-on을 함께 사용하여 양방향 바인딩 -->
        <input :value="text" @input="onInput">
        <!-- v-model을 사용하여 양방향 바인딩 -->
        <!-- <input v-model="text"> -->

        <p>{{ text }}</p>

    </div>
</template>
<script>
export default {
    data() {
        return {
            text: ''
        }
    },
    methods: {
        // 네이티브 DOM 이벤트를 인자로 받는다.
        onInput(e) {
            this.text = e.target.value
        }
    }
}
</script>
<style>
    
</style>