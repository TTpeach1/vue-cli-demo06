<template>
  <div>
    <van-button square type="primary" class="zuo" @click="comName='MP01'">手机注册</van-button>
    <van-button square type="primary" class="you" @click="comName='MP02'">邮箱注册</van-button>
    
    <keep-alive>
      <component :is="comName">
        <!-- <template v-slot:address='rad'>
            <van-radio-group v-model="rad.radio" direction="horizontal">
            <van-radio name="1">中国大陆</van-radio>
            <van-radio name="2">中国香港</van-radio>
            </van-radio-group>
        </template> -->
      </component>
    </keep-alive>
  </div>
</template>

<script>
import MP01 from '@/components/MP01';
import MP02 from '@/components/MP02';
export default {
    data(){
        return{
            comName: "MP01",
        }
    },
    components: {
        MP01,MP02
    }
}
</script>

<style>
body{
    background-color: #f5f5f5;
}
.zuo{ 
    width: 50%;
}
.you{
    width: 50%;
}
</style>