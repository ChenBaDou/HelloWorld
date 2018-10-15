/**
 * ============================
 * @Author:   ChenBaDou
 * @Version:  1.0 
 * @DateTime: 2018.09.06
 * ============================
 */
<template>
    <div class="main">
        {{msg}}
    </div>
</template>
<style src="" scoped lang="sass-loader"></style>
<script>
    export default{
        data(){
            return {
                msg: "HELLO WORLD"
            }
        },
        methods: {},
        created(){
            console.log("index created");
        },
        mounted(){
            console.log("index mounted");
        },
        computed: {
        },
        beforeDestroy(){
            console.log("index beforeDestroy");
        },
        components: {}
    }
</script>