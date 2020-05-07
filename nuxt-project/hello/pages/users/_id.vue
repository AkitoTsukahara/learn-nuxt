<template>
    <div class="container">
        <p>{{ message }}</p>
        <p>ID : {{ this.$route.params.id }}</p>
    </div>
</template>

<script>
    export default {
        data: function () {
            return {
                message: '/users/_id.vueを表示中'
            }
        },
        validate({ params }){
            return /^\d+$/.test(params.id)
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
