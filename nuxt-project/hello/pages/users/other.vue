<template>
    <div class="container">
        <h1>TOP</h1>
        <p>{{ message }}</p>
        <hr>
        <router-link to="/price">link to price</router-link>
    </div>
</template>

<script>
    export default {
        data: function () {
            return {
                message: 'Hello World!'
            }
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
