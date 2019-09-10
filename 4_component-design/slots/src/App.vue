<template>
<div>
  <ul>
    <list-item style="color:red;">
      item1
    </list-item>
    <list-item>
      <p>item 2</p>
      <span>hello</span>
    </list-item>
  </ul>
  <!-- <list-item item="item1" ></list-item>
  <list-item item="item2" ></list-item>
  <list-item item="item3" ></list-item> -->
</div>
  
</template>

<script>
 import ListItem from './components/ListItem.vue';
 
  export default {
    components:{
      'list-item': ListItem,
    }
  };
</script>

<style lang="scss" scoped>

</style>