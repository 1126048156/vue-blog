<template>
    <div class="searchbox" v-show="isShow">
      <div class="search">
        <form action="#" method="post" name="searchform" id="searchform">
          <input name="keyboard" id="keyboard" class="input_text" :value=kw :style=style @focus="focus" @blur="blur" type="text">
          <input name="show" value="title" type="hidden">
          <input name="tempid" value="1" type="hidden">
          <input name="tbname" value="news" type="hidden">
          <input name="Submit" class="input_submit" value="搜索" type="submit">
        </form>
      </div>
      <div class="searchclose" @click="close"></div>
    </div>
</template>

<script>
  import { eventBus } from '../main'
  export default {
        name: "Search",
        data() {
            return {
              kw:"请输入关键字词",
              style:"color: rgb(153, 153, 153);",
              isShow:false
            }
        },
        created(){
          eventBus.$on('show',(msg)=>{
            this.isShow = msg;
          })
        },
      methods:{
          focus(){
            if(this.kw == '请输入关键字词'){
              this.style='color:#000;';this.kw=''
            }
          },
          blur(){
            if(this.kw==''){this.style='color:#999;';this.kw='请输入关键字词'}
          },
        close(){
            this.isShow = false;
            eventBus.$emit("close",this.isShow);
        }
      }
    }
</script>

<style scoped>

</style>
