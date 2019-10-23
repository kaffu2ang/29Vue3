<template>
    <div class="page2">
        <h3>2.选择你的兴趣爱好</h3>
        <p>
            <input type="checkbox" value="看片" v-model="checkbox"><label>看片</label>
            <input type="checkbox" value="游泳" v-model="checkbox"><label>游泳</label>
            <input type="checkbox" value="跑步" v-model="checkbox"><label>跑步</label>
            <input type="checkbox" value="看电影" v-model="checkbox"><label>看电影</label>
            <input type="checkbox" value="听音乐" v-model="checkbox"><label>听音乐</label>
            <input type="checkbox" value="动漫" v-model="checkbox"><label>动漫</label>
        </p>

        <p><router-link to="/page1">上一步</router-link><router-link to="/page3" @click.native="doClick2">下一步</router-link><a href="#" @click="del()">重置</a> </p>

    </div>
</template>

<script>
    export default {
        name: "Page2",
        data(){
            return {
               checkbox:[]
            }
        },
        methods:{
            doClick2(){
                alert(this.checkbox);
                this.$store.commit("addList",this.checkbox)
            },
            del(){
                this.checkbox=[]
            }
        }
    }
</script>

<style scoped>



</style>