<template>
    <div class="home">
        <div class="file-wrap">
        <span class="btn openFontFile">
            导入font文件
            <input type="file" id="fileload" v-on:change="preview"/>
        </span>
        </div>
        <!--常用文字填写区域-->
        <h3 class="title mt10">填写常用文字</h3>
        <div class="font-wrap mt10">
            <textarea id = 'txt'></textarea>
        </div>
        <!--预览区域-->
        <h3 class="title mt10">预览</h3>
        <div class="preview mt10">
            <p class="font-0">这是预览字体</p>
            <p class="font-1">这是预览字体</p>
            <p class="font-2">这是预览字体</p>
        </div>
        <div class="bottom-wrap">
            <!-- <button class="btn generate" id="generateBtn" v-on:click="generate">生成</button> -->
            <!-- <el-button>生成</el-button>    -->
        </div>
    </div>
</template>

<script>
    import { Button } from 'element-ui'
    export default {
        name: 'home',
        methods: {
            generate () {
                alert('生成')
            },
            preview () {
                alert('预览')
            }
        },
        component: {
            elButton: Button
        }
    }
</script>

<style lang="scss" scoped>
    .mt10{
        margin-top: 10px!important;
    }

    .btn{
        border-radius: 4px;
        background-color: #4A90E2;
        &:focus, &:active{
            opacity: 0.5;
        }
    }
    .title{
        padding: 0 10px;
        font-size: 16px;
        color: #666;
    }
    .file-wrap{
        padding-top: 50px;
        text-align: center;
        .openFontFile{
            position: relative;
            display: inline-block;
            height: 30px;
            width: 100px;
            color: #fff;
            line-height: 30px;
            input[type="file"]{
                display: block;
                position: absolute;
                left: 0;
                top: 0;
                width: 100%;
                height: 100%;
                opacity: 0;
            }
        }
    }
    .font-wrap{
        padding: 0 10px;
        textarea{
            display: block;
            width: 100%;
            height: 100px;
        }
    }
    .preview{
        padding: 0 10px;
        .font-0{
            font-size: 12px;
        }
        .font-1{
            font-size: 16px;
        }
        .font-2{
            font-size: 20px;
        }
    }

    .bottom-wrap{
        position: fixed;
        width: 100%;
        bottom: 0;
        left: 0;
        text-align: center;
        .generate{
            display: inline-block;
            height: 60px;
            width: 100%;
            color: #fff;
            line-height: 60px;
            font-size: 24px;
            border: 0 none;
        }
    }
</style>