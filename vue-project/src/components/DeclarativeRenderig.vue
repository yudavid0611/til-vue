<template lang="">
    <div>
        <h2>{{ message }}</h2>
        
        <!-- JS 표현식 또한 적용할 수 있다. -->
        <h2>{{ message.split('').reverse().join('') }}</h2>
    </div>
</template>

<script>
export default {
    // 컴포넌트에서 객체를 반환하는 함수 data 옵션으로
    // 반응형 상태를 선언할 수 있다.
    data() {
        return {
            message: 'Hello Vue3 !'
        }
    }
}
</script>

<style lang="">
    
</style>