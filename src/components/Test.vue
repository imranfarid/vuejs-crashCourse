<template>
    <div class="test">
        <!-- <span v-html="title"> </span> -->
        <h1>{{title}}</h1>
        <p>{{user.first_name}}</p>
        <p v-text="user.first_name"></p>
    </div>
</template>

<script>
    export default{
        name: 'test',
        data(){
            return{
                title: 'Hello World',
                user: {
                    first_name: 'Imran',
                    last_name: 'Farid'
                }
            }
        }
    }
</script>

<style scoped>
</style>
