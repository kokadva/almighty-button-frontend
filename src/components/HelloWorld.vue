<template>
    <div class="hello">
        <button v-on:click="onSendMailButtonClick">Send</button>
    </div>
</template>

<script>

    import axios from 'axios';

    export default {
        name: 'HelloWorld',
        data() {
            return {
                message: "test"
            }
        },
        props: {
            msg: String
        },

        methods: {
            onSendMailButtonClick() {
                axios.get('https://almighty-button-main-server.herokuapp.com/')
                    .then(() => {
                        alert("Message sent")
                    })
            }

        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    h3 {
        margin: 40px 0 0;
    }

    ul {
        list-style-type: none;
        padding: 0;
    }

    li {
        display: inline-block;
        margin: 0 10px;
    }

    a {
        color: #42b983;
    }
</style>
