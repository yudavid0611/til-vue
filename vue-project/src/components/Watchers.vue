<template>
    <div>
        <p>할 일 id: {{ todoId }}</p>
        <button @click="todoId++">다음 할 일 가져오기</button>
        <p v-if="!todoData">로딩...</p>
        <pre v-else>{{ todoData }}</pre>
    </div>
</template>
<script>
export default {
    data() {
        return {
            todoId: 1,
            todoData: null,
        }
    },
    methods: {
        async fetchData() {
            this.todoData = null
            const res = await fetch(
                `https://jsonplaceholder.typicode.com/todos/${this.todoId}`
            )
            this.todoData = await res.json()
        }
    },
    mounted() {
        this.fetchData()
    },
    // watch 옵션으로 todoId 속성 변경 시 side effect를 수행
    watch: {
        todoId() {
            this.fetchData()
        }
    }
}
</script>
<style>
    
</style>