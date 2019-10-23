<template>

    <div class="page1">

        <h3>1.请问您的性别是</h3>
        <input name="man" type="radio" value="男" v-model="checked" />男
        <input name="woman" type="radio" value="女" v-model="checked"/>女
        <input name="m" type="radio" value="保密" v-model="checked"/>保密
        <p><router-link to="/page2" @click.native="doClick">下一步</router-link><a href="#" @click="del()">重置</a> </p>


    </div>
</template>

<script>
    export default {
        name: "Page1",
        data(){
            return {
               checked: ""
            }
        },
        methods:{
            doClick(){
                alert(this.checked);
                this.$store.commit("addSex",this.checked)
            },
            del(){
                this.checked='保密'
            }
        }
    }
</script>

<style scoped>

input[type='radio']{
        padding:10px 20px;
       font-size:18px;
}

</style>