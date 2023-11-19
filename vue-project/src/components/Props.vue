<template>
    <div>
        <h2>{{ msg || 'prop이 아직 전달되지 않았습니다!' }}</h2>
    </div>
</template>
<script>
export default {
    // 부모로부터 받을 데이터 정의
    props: {
        msg: String,
    }
}
</script>
<style>
    
</style>