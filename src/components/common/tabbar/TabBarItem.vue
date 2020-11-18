<template>
    <div class="tab-bar-item" @click="toPage">
      <div v-if="!isActive">
        <slot name="tab-bar-item-icon"></slot>
      </div>
      <div v-else>
        <slot name="tab-bar-item-icon-active"></slot>
      </div>
      <div :style="active">
        <slot name="tab-bar-item-text"></slot>
      </div>
    </div>
</template>

<script>
export default {
  name: "TabBarItem",
  props:{
    path:String,
    activeColor:{
      type:String,
      default:"deepPink"
    }
  },
  data(){
    return{
      //isActive:true
    }
  },
  computed:{
    isActive(){
      return this.$route.path.indexOf(this.path)!==-1
    },
    active(){
      return this.isActive?{color:this.activeColor}:{}
    }
  },
  methods:{
    toPage(){
   //  if(this.$route.path.indexOf(this.path)!==-1){
       this.$router.replace(this.path)
  //   }
    }
  },
}
</script>

<style scoped>
.tab-bar-item{
  flex: 1;
  text-align: center;
  height: 49px;
  font-size: 12px;
}
.tab-bar-item img{
  height: 24px;
  width: 24px;
  margin-top: 3px;
  vertical-align: middle;
}
/*.active{*/
/*  color: #fc8b8b;*/
/*}*/
</style>
