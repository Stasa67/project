<template>
<div class="result">
  <BankComponent v-for="(item, index) in bank" :items="item.items" :img="item.img" :beaver="item.beaver" :key="index" />
</div>
</template>

<script>
import BankComponent from './components/Bank.vue'

export default {
  name: 'App',
  components: {
    BankComponent
  },
  computed: {
    bank: function () {
      return [{
        img: "https://i.pinimg.com/736x/e2/ed/76/e2ed7679ae3d8421fe97def95ffde02e.jpg",
        beaver: true ,
        items: this.items1
      },{
        img: "https://static-cse.canva.com/blob/584144/.png",
        beaver: false,
        items: this.items2
      },{
        img: "https://wl-adme.cf.tsp.li/resize/728x/jpg/8c7/9eb/0a12375a07b5df30df2c696af2.jpg",
        beaver: true,
        items: this.items3
      }
    ]
    },
    items1: function () {
      return [
      {
        title: "прозрачные условия"
      },{
        title: "входит в АВС"
      },
      {
        title: "есть лицензия Банка РФ"
      },
      {
        title: "честный договор"
      }
    ]
    },
    items2: function () {
      return [
      {
        title: "непрозрачные условия"
      },{
        title: "входит в АВС"
      },
      {
        title: "есть лицензия Банка РФ"
      },
      {
        title: "фактический процент меньше"
      }
    ]
    },
    items3: function () {
      return [
      {
        title: "самые выгодные условия"
      },{
        title: "лицензия отозвана"
      },
      {
        title: "плохой договоp"
      },
      {
        title: "реклама на сайте"
      }
    ]
    }
  }
}
</script>

<style>

</style>
