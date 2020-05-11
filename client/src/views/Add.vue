<template>
  <div>
        <van-uploader
            :mix-count='1'
            :after-read="afterRead"
            v-model="fileList"
        />
        <van-cell-group>
            <van-field
                label="文章标题"
                placeholder="文章标题"
                v-model="title"
            />

            <van-field
                label="文章简介"
                placeholder="文章简介"
                v-model="summary"
            />

            <van-field
                label="文章内容"
                placeholder="文章内容"
                v-model="content"
                type="textarea"
                autosize="autosize"
            />
        </van-cell-group>
        <van-button type="primary" @click="handeAdd" class="add-button">提交</van-button>
  </div>
</template>

<script>
import { Uploader, CellGroup, Field, Button  } from 'vant'

export default {
    components: {
        [Uploader.name]: Uploader,
        [CellGroup.name]: CellGroup,
        [Field.name]: Field,
        [Button.name]: Button
    },
    data() {
        return {
            fileList: [],
            title: '',
            summary: '',
            content: '',
            img: ""
        }
    },
    methods: {
        afterRead(info){
            this.img = info.content
        },
        handeAdd(){
            const data = {
                title: this.title,
                summary: this.summary,
                content: this.content,
                img: this.img,
            }
            console.log(data)
        }
    }
}
</script>

<style>

</style>