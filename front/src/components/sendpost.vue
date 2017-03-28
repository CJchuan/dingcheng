<template>
    <div class="sendpost">
      <div class="header2">
            <left></left>
            <h2>发表帖子</h2>
      </div>
      <Writecont></Writecont>
      <mt-button type="primary" @click="sendpost">发表</mt-button>
    </div>
</template>

<script>
import left from "./left.vue";
import Writecont from "./Writecont.vue";
    export default {
        name:'sendpost',
        data(){
            return{

            }
        },
        components:{
                Writecont,
                left
        },
        methods:{
          sendpost(){
            this.$http.get("http://10.2.158.246:3000/posts/write",{userId:1,username:"yzx",word:"今天天气好！",}).then(res=>{

            })
          }
        }
    }
</script>

<style scoped>
  .header2{
        height:4rem;
        line-height:4rem;
        color:#bc9461;
        border-bottom:.1rem solid #ccc;
    }
    .header2 h2{
        text-align:center;
        display:inline-block;
    }
</style>