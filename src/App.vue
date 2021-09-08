<template>
<!-- 親コンポーネント -->
  <div id="app">
      <!-- 子コンポーネントにtitleとmessageに値を入れデータを渡す -->
      <!-- props名の前にv-bind:を付けることで変数を扱えるようになる -->
      <!-- オブジェクト内のオブジェクトを指定する時は「.」で繋げる -->
      <quiz title="問題" message="Question / v-bind無し"/>
      <answer title="A" v-bind:message="select.A"/>
      <answer title="B" v-bind:message="select.B"/>
      <answer title="C" v-bind:message="select.C"/>
      <answer title="D" v-bind:message="select.D"/>

      <!-- 同じ変数名に違う値を入れて子に渡しているが、別の物として同じく表示してくれる -->

  </div>
</template>

<script>
import Answer from './components/answer.vue'
import Quiz from './components/quiz.vue'

// 使いたいコンポーネントをインポートする

// コンポーネントを更に追加する場合は下へそのまま追加する



export default {
  name: 'App',
  components: {
    Quiz,
    Answer
    // 使いたいコンポーネント名を入れる。
  },
  data(){
    return{
      // 変数の作成。v-bindを使い変数を扱う
      Question:"テスト",
      // 配列のようにオブジェクトの中にオブジェクトを作る形
      // select配列のAみたいに考える
      select:{
        A:"AAAA",
        B:"BBBB",
        C:"CCCC",
        D:"DDDD"
      }
    }
  },
};
</script>
