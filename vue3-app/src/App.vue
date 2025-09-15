<!-- vbc 입력 후 Enter => 전체 템플릿 입력됨 -->
<!-- vda 입력 후 Enter => data() 부분 자동 작성 -->
 <!-- 
    >> 축약어
     v-bind:class => :class
     v-on:click   => @click
 -->

<template>
  <AppHeader 
    v-bind:appTitle="message"
    v-on:change="changeMessage">
  </AppHeader>
  <!-- <div>
    {{ message }}
  </div>
  <button @click="showAlert">경고</button> -->
</template>

<script>
  // import 컴포넌트이름 from './컴포넌트 경로'
  import AppHeader from './components/AppHeader.vue';

  export default {
    components:{
      // '컴포넌트 이름': 컴포넌트 내용
      // 'app-header': AppHeader
      // 'AppHeader': AppHeader
      // AppHeader: AppHeader
      AppHeader
    },
    data() {
      return {
        message: '앱 헤더 컴포넌트'
      }
    },
    methods:{
      changeMessage(){
        this.message = '변경됨'
      }
    }
  }
</script>

<style scoped>

</style>