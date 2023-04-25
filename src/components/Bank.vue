<template>
<div class="result">
  <div class="result-avatar">
    <img :src="img" class="result-avatar__img">
  </div>
  <div class="result-factor">
    <div class="result-factor__item" v-for="item in items" :key="item.title">{{ item.title }}</div>
  </div>
  <div class="result-beaver" v-if="beaver">
    <img class="result-beaver__img" src="https://img.freepik.com/premium-vector/cute-cartoon-beaver-reading-a-book_290315-1403.jpg">
  </div>
</div>
</template>

<script>
export default {
  name: 'BankComponent',
  props: {
    title: Storage,
    img: String,
    beaver: Boolean,
    items: Array
  }
}
</script>


<style>
.result {
  margin-top: 20px;
  width: 860px;
  height: 158px;
  background: #4e63d980;
  border-radius: 30px;
}

.result-avatar {
  position: absolute;
  width: 70px;
  height: 70px;
  margin: 14px 0 0 20px;
  border-radius: 100%;
  background: #F2F2F2;
}

.result-factor {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  padding-left: 162px;
  padding-right: 60px;
}

.result-factor__item {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 214px;
  height: 40px;
  margin: 20px;
  background: #5c6273bf;
  border-radius: 30px;
  color: #F2F2F2;
}

.result-avatar__img {
  display: flex;
  width: 70px;
  height: 70px;
  border-radius: 100%;
  align-items: center;
}

.result-beaver {
  position: absolute;
  transform: rotate(346deg);
  top: 46px;
  left: 720px;
  width: 140px;
  height: 140px;
}

.result-beaver__img {
  width: 140px;
  height: 140px;
}

</style>
