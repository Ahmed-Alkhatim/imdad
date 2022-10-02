<template>
    <div class="message" v-for = "messges in messages">
        <div class="message-img">
            <img :src= "user" alt= "profile"/>
        </div>
        <div class="chater" >
            <h2>{{messges.name}}</h2>
            <p>{{messges.last_message}} <span>2</span></p>
        </div>
    </div>
     
</template>

<script setup>
    import { onMounted } from 'vue';
    const props = defineProps(["messages"])

    onMounted( () => {
        console.log("Hello World")
    })

</script>

<style lang="scss" scoped>

</style>