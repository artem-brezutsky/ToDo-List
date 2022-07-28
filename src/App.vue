<template>
    <div>
        <button v-on:click="addlike">Like</button>
        <button v-on:click="addDisLike">DisLike</button>
    </div>
    <div>Кол-во лайков <strong>{{ likes }}</strong></div>
    <div>Кол-во дизлайков <strong>{{ disLikes }}</strong></div>
</template>

<script>
export default {
    data() {
        return {
            likes: 0,
            disLikes: 5,
        }
    },
    methods: {
        addlike() {
            this.likes++
        },
        addDisLike() {
            this.disLikes++
        },
    },  
}
</script>

<style>

</style>