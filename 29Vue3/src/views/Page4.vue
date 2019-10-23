<template>
    <div class="page4">

        <p> 您的性别是:{{sex4}}</p>
        <p> 您的爱好是:<span v-for="(item,index) in list4" :key="index">{{item}}</span></p>
        <p> 个人简介:{{this.$store.state.text}}</p>

    </div>
</template>

<script>
    export default {
        name: "Page4",
        data(){
            return {
　　　　　　　　 sex4: this.$store.state.sex,
                list4:this.$store.state.list,
                text4: this.$store.state.text
            }
        }



    }
</script>

<style scoped>


</style>