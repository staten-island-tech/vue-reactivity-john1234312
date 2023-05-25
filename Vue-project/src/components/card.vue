<template>
    <div class="card" :id="image">
        <h2>{{ title }}</h2>
        <img :src="image" alt="" />
        <p>{{ description }}</p>
        <button @click="addStorage">Add Book</button>
    </div>
</template>

<script>
export default {
    name: "card",
    props: {
        title: String,
        description: String,
        image: String,
        addStorage: Function,
    },
};
</script>

<style scoped>
    img {
        height: 500px;
        width: 500px;
    }
</style>