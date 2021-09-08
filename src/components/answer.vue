<template>
  <div class="alert alert-info">
    <h1>{{ title }}</h1>
    <hr>
    <h3>{{ message }}</h3>

    <div>

      <button class="btn btn-info mt-2" v-on:click="doAction">
        Click
      </button>
    </div>
  </div>
</template>

<script>
export default{
  name: 'answer',
  props: {
    title: String,
    message: String,
  },
  methods:{
    doAction(){
      //送信ボタンを押したらinput内のデータにmessageを「no name」から書き換える
      if(this.title === 'D'){
          console.log('正解');
      }else{
          console.log('不正解');
      }
    }
  }
}
</script>
