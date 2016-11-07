<template>
    <div>
        <p>{{ message }}</p>
        {{ data }}
    </div>
</template>
<script>
export default{
    data() {
        return{
            message : 'it\'s all foobar',
            data: {}
        }
    },
    created() {
        console.log('ready');
        this.getFoo();
    },

    methods: {
        getFoo: function() {
            console.log('fetching')
            fetch('https://radiant-ridge-45919.herokuapp.com/times').then(response => {
                response.json().then(res => {
                    console.log(res);
                    this.data = res;
                })

            })
        }
    }
}
</script>
<style>
</style>