<template>
  <div>
      <van-list
        v-model="loading"
        :finished="finished"
        finished-text="没有更多了"
        @load="onLoad"
      >
        <van-cell v-for="item in list" :key="item.id" @click="handClick(item.id)">
            <div class="list">
                <div class='left'> 
                    <img :src="item.img" />
                </div>
                <div class='right'> 
                    <div class="title">{{item.title}}</div>
                    <div class="create-time">{{item.createTime}}</div>
                </div>
            </div>
        </van-cell>
      </van-list>
  </div>
</template>

<script>

import { List, Cell } from 'vant'

export default {
  components:{
    [List.name]: List,
    [Cell.name]: Cell
  },
  data(){
    return{
      loading: false,
      finished: false,
      list: []
    }
  },
  methods: {
    onLoad(){
        setTimeout(() => {
          this.loading = false,
          this.finished = true,
          this.list = [
            {
              id: '1',
              img: 'https://img.yzcdn.cn/vant/logo.png',
              title: 'adasdasdasd1',
              createTime: 'asdasdasdasdasdas'
            },
            {
              id: '2',
              img: 'https://img.yzcdn.cn/vant/logo.png',
              title: 'adasdasdasd2',
              createTime: 'asdasdasdasdasdas'
            },
            {
              id: '3',
              img: 'https://img.yzcdn.cn/vant/logo.png',
              title: 'adasdasdasd3',
              createTime: 'asdasdasdasdasdas'
            },
            {
              id: '4',
              img: 'https://img.yzcdn.cn/vant/logo.png',
              title: 'adasdasdasd4',
              createTime: 'asdasdasdasdasdas'
            },
            {
              id: '5',
              img: 'https://img.yzcdn.cn/vant/logo.png',
              title: 'adasdasdasd4',
              createTime: 'asdasdasdasdasdas'
            },
            {
              id: '6',
              img: 'https://img.yzcdn.cn/vant/logo.png',
              title: 'adasdasdasd4',
              createTime: 'asdasdasdasdasdas'
            },
            {
              id: '7',
              img: 'https://img.yzcdn.cn/vant/logo.png',
              title: 'adasdasdasd4',
              createTime: 'asdasdasdasdasdas'
            }
          ]
        },1000)
    },
    handClick(id){
      this.$router.push({
        path: '/detail',
        query: {
          id
        }
      })
    }
  }
}
</script>

<style scoped>
  .list{
    display: flex;
    flex-direction: row;
  }
  .list .left, img{
    width: 150px;
    height: 100px;
    border-radius: 10px;
  }
  .list .right{
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    margin-left: 20px;
  }
  .list .right .title{
    font-size: 18px;
  }
  .list .right .create-time{
    font-size: 12px;
    color: #9e9e9e;
  }

    

</style>