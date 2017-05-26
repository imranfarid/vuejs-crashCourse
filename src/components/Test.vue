<template>
    <div class="test">
        <input type="text" v-model="title"><br/>
        <!-- <span v-html="title"> </span> -->
        <h1>{{title}}</h1>
        <p v-if="showName">{{user.first_name}}</p>
        <p v-else>{{user.last_name}}</p>
        <ul>
            <li v-for="item in items">{{item.title}}</li>
        </ul>
        <button v-on:click="greet('Hello World')">Say greeting</button><br />
        <input type="text" v-on:keyup="pressKey" v-on:keyup.enter="enterHit">
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
                showName: true,
                items: [
                    {title: 'Item One'},
                    {title: 'Item Two'},
                    {title: 'Item Three'},
                ]
            }
        },
        methods: {
            greet: function(greeting){
                alert(greeting);
            },
            pressKey: function(e){
                console.log(e.target.value);
            },
            enterHit: function(){
                console.log('You hit enter')
            }
        }
    }
</script>

<style scoped>
</style>
