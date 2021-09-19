<template>
  <div>
<form @submit.prevent="onSubmit">
<input type="text" v-model="text" placeholder="Search Jokes..."/>
<input type="submit" value="Search Jokes"/>
</form>
  </div>
</template>

<script>
  export default {
    name:'searchJokes',
    data(){
      return{
         text:''
      }
    },
    methods:{
      onSubmit(){
this.$emit('search-text',this.text);
this.text="";
      }
    }
  }
</script>

<style lang="css" scoped>

</style>
