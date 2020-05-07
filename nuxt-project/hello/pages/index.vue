<template>
    <div class="container">
        <h1>TOP</h1>

         <div>
<!--             <p>{{ $store.state.message }}</p>-->
             <p>{{ $store.state.hello.message }}</p>
<!--             <button v-on:click="$store.commit('updateMessage','Commit with payload')">Update</button>-->
<!--             <button v-on:click="$store.dispatch('updateMessageAction','Dispatch with payload')">Dispatch</button>-->
             <button v-on:click="$store.dispatch('hello/updateMessageAction','Dispatch with payload')">Dispatch</button>
         </div>


        <table>
            <tbody>
            <tr>
                <th>ID</th>
                <th>NAME</th>
                <th>COMPANY</th>
            </tr>
            <tr v-for="user in users" :key="user.id">
                <td>{{ user.id}}</td>
                <td>{{ user.name}}</td>
                <td>{{ user.company.name}}</td>
            </tr>
            </tbody>
        </table>
        <hr>
        <router-link to="/price">link to price</router-link>
    </div>
</template>

<script>
    const axios = require('axios')
    let url ='https://jsonplaceholder.typicode.com/users'

    export default {
        asyncData({ params, error }){
            return axios.get(url)
                .then((res) => {
                    return { users: res.data }
                })
                .catch(( e => {
                    error({ users: e.response.status, message: e.message })
                }))
        }
    }
</script>

<style>
    .container {
        margin: 100px auto;
        min-height: 100vh;
        display: block;
        justify-content: center;
        align-items: center;
        text-align: center;
    }

    .title {
        font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
        'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
        display: block;
        font-weight: 300;
        font-size: 100px;
        color: #35495e;
        letter-spacing: 1px;
    }

    .subtitle {
        font-weight: 300;
        font-size: 42px;
        color: #526488;
        word-spacing: 5px;
        padding-bottom: 15px;
    }

    .links {
        padding-top: 15px;
    }
</style>
