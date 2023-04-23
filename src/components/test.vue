<template>
    <div class="test">
        {{ msg }}
    </div>
</template>

<script>
    export default{
        data(){
            return {
                title: "Hello vue",
                user: {
                    name: "Maria",
                    lastname: "Jose"
                },
                myhtml: '<h3>vue</h3>',
                showName: true,
                tasks: [
                    {title: "eat"},
                    {title: "sleep"},
                    {title: "play"},
                    {title: "sing"},
                ]
            }
        },
        methods: {
            saludar(name){
                alert('Hello ' + name)
            },
            typingEnter(e){
                console.log('Dio un enter');
            }
        },
        computed:{
            fullname(){
                return this.user.name + ' ' + this.user.lastname
            }
        },
        props: {
            msg: {
                type: String,
                default: "mensaje por defecto"
            }
        }
    }
</script>

<style media="screen">
    .test{
        background: #202020;
        color: aliceblue;
    }
</style>