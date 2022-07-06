<template>
  <div>
    <MS>
        <template v-slot:id='scope'>
        <p>{{scope.row+1}}</p>
      </template>
      <template v-slot:name='scope'>
        <input type="text" v-model="scope.row.name">
      </template>
      <template v-slot:age='scope'>
        <input type="text" v-model="scope.row.age">
      </template>
      <template v-slot:headImgUrl='scope'>
        <img :src="scope.row.headImgUrl" alt="" >
      </template>
    </MS>
  </div>
</template>

<script>
import MS from '@/components/MS'
export default {
    components:{
        MS,
    }
}
</script>

<style>

</style>