<template>
  <div>
    <!-- 注册页面 -->
      <MyPhone></MyPhone>
      <hr>
    <!-- 学生渲染 -->
      <MyStudent></MyStudent>
  </div>  
</template>
<script>
import MyPhone from '@/views/MyPhone';
import MyStudent from '@/views/MyStudent'
export default {
  components: {
    MyPhone,
    MyStudent,
  },
};
</script>

<style></style>
