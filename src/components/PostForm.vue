<template>
    <form @submit.prevent>
        <h1>Создание поста</h1>
        <input v-model="post.title" class="input" type="text" placeholder="Название">
        <input v-model="post.body" class="input" type="text" placeholder="Описание">
        <my-button class="btn" @click="createPost"></my-button>
    </form>
</template>
    
<script>
import MyButton from "@/components/UI/MyButton.vue"
export default {
    components: {MyButton},
    data() {
        return {
            post: {
                title: '',
                body: ''
            }
        }
    },
    methods: {
        createPost() {
            this.post.id = Date.now();
            this.$emit('create', this.post)
            this.post = {
                title: '',
                body: ''
            }
        }
    }

}
</script>
    
<style scoped>
form {
    display: flex;
    flex-direction: column;
}

.input {
    width: 100%;
    padding: 10px 15px;
    margin: 10px 0;
    border: 1px solid teal;
}
</style>