<template>
    <el-upload
            class="upload-demo"
            drag
            action="http://localhost:80/upload/image"
            :on-success="handleAvatarSuccess"
            multiple>
        <i class="el-icon-upload"></i>
        <div class="el-upload__text">将文件拖到此处，或<em>点击上传</em></div>
        <div class="el-upload__tip" slot="tip">只能上传jpg/png文件，且不超过50M</div>
    </el-upload>
</template>

<script>
    export default {
        name: "Test",
        data(){
            return{
                avatar:"",
            }
        },
        methods:{
            handleAvatarSuccess(res) {
                // res就是文件的路径
                console.log(res);
                this.avatar = res
            }
        }
    }
</script>

<style>

</style>