<template>
    <div>
      <h1>日記一覧</h1>
      <ul v-if="diaries.length > 0">
        <li v-for="diary in diaries" :key="diary.id">
          <h3>{{ diary.title }}</h3>
          <p>{{ diary.content }}</p>
        </li>
      </ul>
      <p v-else>日記がありません。</p>
    </div>
  </template>
  
  <script>
  import axios from "axios"; // API 通信用ライブラリ
  
  export default {
    data() {
      return {
        diaries: [], // API から取得したデータを入れる配列
      };
    },
    mounted() {
      // Vue のライフサイクル「mounted」で API を呼ぶ
      axios.get("http://localhost:8080/api/diaries")
        .then(response => {
          this.diaries = response.data; // API から取得したデータをセット
          console.log(this.diaries); // 配列の中身を確認
        })
        .catch(error => {
          console.error("APIエラー:", error);
        });
    }
  };
  </script>
  
  <style scoped>
  h1 {
    color: #333;
  }
  ul {
    list-style-type: none;
    padding: 0;
  }
  li {
    padding: 10px;
    border-bottom: 1px solid #ddd;
  }
  </style>
  