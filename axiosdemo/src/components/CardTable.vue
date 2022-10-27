<template>
  <div>
    <el-table :data="cards" style="width: 100%">
    <el-table-column prop="id" label="id" width="180" />
    <el-table-column prop="name" label="卡牌" width="180" />
    <el-table-column prop="win_rate" label="胜率" />
    <el-table-column prop="exist_rate" label="存在率" />
    <el-table-column prop="num_ave" label="平均携带张数" />
    <el-table-column prop="deck_win" label="卡组胜率" />
  </el-table>
  <div class="example-pagination-block">
    <div class="example-demonstration">When you have few pages</div>
    <el-pagination layout="prev, pager, next" :total="50" />
  </div>
  </div>
</template>

<script>

export default {
  name: 'HelloWorld',
  // props: {cards:String},
  data(){
    return{
      cards:[]
    }

  },
  mounted(){
    let page = 4
    let api = "http://127.0.0.1:8000/auea/?page="+page
    this.axios.get(api).then((res)=>{
      console.log(res)
      this.cards = res.data.results
      console.log(res)

      // let api = "https://api.hearthstonejson.com/v1/95431/zhCN/cards.json"
      // this.axios.get(api).then((res)=>{
      // console.log(res)
      // this.cards = res.data
      // console.log(res)
    })
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

