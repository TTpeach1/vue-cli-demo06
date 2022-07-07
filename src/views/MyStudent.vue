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
        <a v-if='scope.row.type==0' :href="scope.row.headImgUrl">{{scope.row.headImgUrl}}</a>
        <img v-else-if='scope.row.type==1' :src="scope.row.headImgUrl" alt="" >
        <div v-else>{{scope.row.headImgUrl}}</div>
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