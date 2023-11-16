<template>
    <div>
        <!-- v-on 디렉티브를 사용하여 DOM 이벤트를 수신할 수 있다. -->
        <!-- <button v-on:click="increment">숫자 세기: {{ count }}</button> -->
        <button @click="increment">숫자 세기: {{ count }}</button>
        
    </div>
</template>
<script>
export default {
    data() {
        return {
            count: 0
        }
    },
    // methods 옵션
    methods: {
        increment() {
            // this를 사용하여 컴포넌트 인스턴스에 접근
            this.count++
        }
    }
}
</script>
<style>
    
</style>