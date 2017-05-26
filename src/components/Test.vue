<template>
    <div class="test">
        <!-- <span v-html="title"> </span> -->
        <h1>{{title}}</h1>
        <p v-if="showName">{{user.first_name}}</p>
        <p v-else>{{user.last_name}}</p>
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
                },
                showName: true
            }
        }
    }
</script>

<style scoped>
</style>
