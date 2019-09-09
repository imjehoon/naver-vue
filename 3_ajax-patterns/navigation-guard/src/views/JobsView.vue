<template>
  <div>
    <!-- TODO: 라우터 네비게이션에서 호출한 액션 함수의 state를 여기에 뿌려보세요. -->
    <!-- TODO: 구직 공고의 목록만 정리하여 출력하면 됩니다 -->
     <li v-for="newsItem in this.$store.state.jobs" v-bind:key="newsItem.id">
        {{ newsItem.title }}
      </li>
  </div>
</template>