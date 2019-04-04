<template>
  <li @click="del">{{content}}</li>
</template>

<script>
export default {
  props:['content','index'],
  methods:{
    del(){
      this.$emit('zidel',this.index);
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
