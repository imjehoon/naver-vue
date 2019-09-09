<template>
  <div>
    <h2>Jobs</h2>
    <ul v-if="!isLoading">
      <li v-for="josbItem in josbItems" v-bind:key="josbItem.id">
        {{josbItem.title}}
      </li>
    </ul>
    <p v-else>loading</p>
  </div>
</template>

<script>
import axios from "axios";

export default {
  data: function(){
    return {
      josbItems: [],
      isLoading: true
    };
  },
  methods: {
    fetchData: function() {
      var vm = this;
      axios.get("https://api.hnpwa.com/v0/jobs/1.json")
        .then(function(response) {
          console.log(response);
          vm.josbItems = response.data;
          vm.isLoading = false;
        })
        .catch(function(error){
          console.log(error);
          
        })
    }
  }, 
  created: function(){
    this.fetchData();
  }
  // TODO: 위 fetchData 메서드를 이용하여 데이터를 받아온 뒤 화면에 구직 공고 제목을 표시해보세요.
};
</script>

<style>
</style>
