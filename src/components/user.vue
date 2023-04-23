<template>
    <div class="user">
        <h1>user components</h1>
        <ul>
            <li v-for="user in users">
                {{ user.name }} - {{ user.email }}
                <button v-on:click="deleteUser(user)">X</button>
            </li>
        </ul>
        <form v-on:submit.prevent="adduser">
            <input type="text" v-model="newuser.name" placeholder="nombre">
            <input type="email" v-model="newuser.email" placeholder="email">
            <button type="submit">Add</button>
        </form>
    </div>
</template>

<script>
export default {
    data() {
        return {
            users: [
                {
                    name: 'joe',
                    email: 'joe@joe.co',
                    contacto: false
                },
                {
                    name: 'maria',
                    email: 'maria@maria.co',
                    contacto: true
                },
                {
                    name: 'javier',
                    email: 'javier@javier.co',
                    contacto: false
                },
            ],
            newuser: {}
        }
    },
    methods:{
        adduser(){
            this.users.push(this.newuser)
            this.newuser = {}
        },
        deleteUser(user){
            this.users.splice(this.users.indexOf(user), 1)
            alert('eliminando')
        }
    }
}
</script>

<style media="screen">
.user {
    background: #333;
    color: aliceblue;
    padding: 20px;
}
</style>