<template>
  <div class="alert alert-info">
    <h1>{{ title }}</h1>
    <hr>
    <h3>{{ message }}</h3>
    <p ref="ansmsg">{{ ans }}</p>

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
  mounted(){
      this.cnt = 0
  },
  methods:{
    doAction(){
      //送信ボタンを押したらinput内のデータにmessageを「no name」から書き換える
      this.cnt++
      if(this.title === 'D' && this.cnt === 1){
          console.log('正解');
          this.$refs.ansmsg.innerHTML += '<h3> ○'
      }else if(this.title !== 'D' && this.cnt === 1){
          console.log('不正解');
      }
    }
  }
}
</script>
