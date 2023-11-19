<template>
    <div>
        <h2>자식 컴포넌트</h2>
    </div>
</template>
<script>
export default {
    emits: ['response'],
    created() {
        this.$emit('response', '자식 컴포넌트로부터 선물 전달!')
    }
}
</script>
<style>
    
</style>