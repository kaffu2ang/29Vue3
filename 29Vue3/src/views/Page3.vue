<template>
    <div class="page3">
        <h3>3.请介绍一下你自己</h3>
        <textarea v-model="text3"></textarea>
        <p>
            <router-link to="/page2">上一步</router-link><router-link to="/page4" @click.native="doClick3">下一步</router-link><a href="#" @click="del()">重置</a>
        </p>

    </div>
</template>

<script>
    export default {
        name: "Page3",
        data(){
            return {
              text3: ''
            }
        },
        methods:{
            doClick3(){
                this.$store.commit("addText",this.text3)
                alert(this.$store.state.text);

            },
            del(){
                this.text3=''
            }
        }
    }
</script>

<style scoped>

    textarea{
        width: 400px;
        height: 200px;
    }

</style>