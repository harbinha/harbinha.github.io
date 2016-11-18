<template>
    <div>
        <p>{{ message }}</p>
    </div>
</template>
<script>
export default{
    data() {
        return{
            message : 'it\'s all foobar',
        }
    },
    created() {
        console.log('ready');
    },

    methods: {}
}
</script>
<style>
</style>