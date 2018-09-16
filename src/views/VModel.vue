<template>
  <div class="v-model">
    <h1>v-model用于组件</h1>
    <base-input v-model='inputValue' @change="inputChange"></base-input>
  </div>
</template>

<script>
import BaseInput from '@/components/BaseInput'
export default {
  components:{
    BaseInput
  },
  data(){
    return {
      inputValue:''
    }
  },
  methods:{
    inputChange(value){
      console.log('changeValue',value)
    }
  }
  
}
</script>

<style lang="sass" scoped>

</style>

