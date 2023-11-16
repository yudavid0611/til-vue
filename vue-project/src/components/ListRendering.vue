<template>
    <div>
        <!-- submit 이벤트 대신 addTodo 메서드 실행 -->
        <form @submit.prevent="addTodo">
            <input v-model="newTodo">
            <button>할 일 추가</button>
        </form>

        <ul>
            <!-- v-for 디렉티브로 자료 배열을 엘리먼트 목록으로 렌더링 -->
            <!-- key를 사용하면 vue가 각 li를 정확하게 이동시켜 배열에서 해당 객체의 위치와 일치하도록 만듦 -->
            <li v-for="todo in todos" :key="todo.id">
                {{ todo.text }}
                <button @click="removeTodo(todo)">제거</button>
            </li>
        </ul>
    </div>
</template>
<script>
// 각 todo에 대한 id
let id = 0

export default {
    data() {
        return {
            newTodo: '',
            todos: [
                { id: id++, text: 'HTML 배우기' },
                { id: id++, text: 'JS 배우기' },
                { id: id++, text: 'Vue 배우기' }
            ]
        }
    },
    methods: {
        addTodo() {
            const newTodoObj = {
                id: id++,
                text: this.newTodo
            }
            // todo 추가
            this.todos.push(newTodoObj)
        },
        removeTodo(target) {
            // target 외의 객체만 포함한 배열 생성
            this.todos = this.todos.filter((todo) => {
                return todo != target
            })
        }
    }
}
</script>
<style>
    
</style>