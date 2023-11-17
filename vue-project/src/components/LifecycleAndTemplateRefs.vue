<template>
    <div>
        <!-- ref 속성으로 템플릿 참조 요청 -->
        <p ref="p">안녕!</p>
    </div>
</template>
<script>
export default {
    // 컴포넌트가 마운트된 후에만 접근할 수 있음
    mounted() {
        this.$refs.p.textContent = 'Mounted!'
    }
}
</script>
<style>
    
</style>