<template>
    <div class="post">
        <div>
            <div><strong>Название: </strong>{{ post.title }}</div>
            <div><strong>Описание: </strong>{{ post.body }}</div>
        </div>
        <div class="post-btn">
            <button>Удалить</button>
        </div>
    </div>
</template>
    
<script>
export default {
    props: {
        post: {
            type: Object,
            required: true,
        }
    }

}
</script>
    
<style scoped>
.post {
    border: 2px solid teal;
    padding: 15px;
    margin-top: 15px;

    display: flex;
    align-items: center;
    justify-content: space-between;
}

</style>