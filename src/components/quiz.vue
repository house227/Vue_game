<template>
<!-- 子コンポーネント -->
  <div class="alert alert-info">
      <!-- 親コンポーネントから受け取った値をそれぞれtitleとmessageへ入れる -->
    <h1>{{ title }}</h1>
      <!-- 渡されたデータは別に表示するが、当然CSS等の適応は一緒にされる-->
    <h4 class="text-primary">{{ message }}</h4>
  </div>
</template>

<script>
export default {
  name: 'quiz',
  props: {
    title: String,
    message: String,
  }
}
</script>
