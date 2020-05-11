<template>
    <div class="detail">
        <div class="title">{{detail.title}}</div>
        <div class="summary">{{detail.summary}}</div>
        <div class="connent">{{detail.concent}}</div>
        <div class="createTime">{{detail.createTime}}</div>
    </div>
</template>

<script>
export default {
    data(){
        return{
            detail: {
              id: '1',
              img: 'https://img.yzcdn.cn/vant/logo.png',
              title: 'List 列表',
              summary: 'summary',
              concent: 'concentconcentconcentconcentconcentconcentconcentconcentconcentconcentconcentconcentconcentconcentconcentconcent',
              createTime: '2020-05-10'
            },
        }
    }
}
</script>

<style scoped>
    .detail{
        padding: 20px;
        text-align: left;
    }
    .detail .title{
        font-size: 20px;
        padding-bottom:20px;
    }
    .detail .summary{
        padding: 20px;
        background: #dcdcdc;
    }
    .detail .connent{
        text-indent: 2em;
        line-height: 200%;
        word-break:break-word;
        padding-top:20px;
    }
    .detail .createTime{
        color: #9c9c9c;
        text-align: right;
    }
</style>