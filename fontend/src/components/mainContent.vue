<template>
    <div class="main-content">
        <div class="banner-div">
            <div class="question-title">
                <p class="question-p">你的提问我来回答 !!! </p>
                <el-button class="question-button"> 我来提问 </el-button>
            </div>
<!--            走马灯效果-->
<!--            <div class="banner">-->
<!--                <div class="block">-->
<!--                    <el-carousel height="150px">-->
<!--                        <el-carousel-item v-for="item in 4" :key="item">-->
<!--                            <h3 class="small">{{ item }}</h3>-->
<!--                        </el-carousel-item>-->
<!--                    </el-carousel>-->
<!--                </div>-->
<!--            </div>-->
        </div>
        <div class="content-div">
            <div class="left-question">
<!--                平台最新问题选择-->
                <div class="select-drop-menu">
                    <span class="plateform">平台最新问题</span>
                    <el-dropdown>
                      <span class="el-dropdown-link">
                        问题类型选择<i class="el-icon-arrow-down el-icon--right"></i>
                      </span>
                      <el-dropdown-menu slot="dropdown">
                        <el-dropdown-item>生活类问题</el-dropdown-item>
                        <el-dropdown-item>学习类问题</el-dropdown-item>
                      </el-dropdown-menu>
                    </el-dropdown>
                    <el-input v-model="input" placeholder="请输入问题类型" class="width-20" clearable></el-input>
                    <el-checkbox v-model="checked" class="float-right">仅看未解决</el-checkbox>
                </div>
                <div class="message-content" v-for="item in 5">
                    <p class=message-title>这是文章的标题</p>
                    <p class="message-main">这是文章的内容这是文章的内容这是文章的内容这是文章的内容这是文章的内容这是文章的内容这是文章的内容
                        这是文章的内容这是文章的内容这是文章的内容这是文章的内容这是文章的内容这是文章的内容这是文章的内容这是文章的内容
                    </p>
                    <p class="message-poster">
                        <span class="el-icon-user-solid">用户甲</span>
                        <span class="margin-20">一个小时前发布</span>
                        <span class="background-green">学习类问题</span>
                        <span class="float-right">查看回答 <span class="el-icon-caret-bottom"></span></span>
                    </p>
                </div>
            </div>
            <div class="right-difference">
                <div class="all-difference">
                    <p>所有分类</p>
                    <hr>
                    <ul>
                        <li><span class="el-icon-question"></span>生活类问题   进入<span class="el-icon-right"></span></li>
                        <li><span class="el-icon-question"></span>生活类问题   进入<span class="el-icon-right"></span></li>
                        <li><span class="el-icon-question"></span>生活类问题   进入<span class="el-icon-right"></span></li>
                        <li><span class="el-icon-question"></span>生活类问题   进入<span class="el-icon-right"></span></li>
                    </ul>
                </div>
                <div class="hot-question">
                    <p>热门问题</p>
                    <hr>
                    <ul>
                        <li><span class="el-icon-user-solid"></span>生活类问题   进入<span class="el-icon-right"></span></li>
                        <li><span class="el-icon-user-solid"></span>生活类问题   进入<span class="el-icon-right"></span></li>
                        <li><span class="el-icon-user-solid"></span>生活类问题   进入<span class="el-icon-right"></span></li>
                        <li><span class="el-icon-user-solid"></span>生活类问题   进入<span class="el-icon-right"></span></li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    'name': 'mainContent',

    data(){
        return {
            "radio":'1',
            // 1生活类问题，2学习类问题
            "questionType":'1',
            "input":'生活类问题',
            "checked":false
        };
    },
    "methods":{
        handleCommand(type){
            this.questionType = type;
        }
    }
};
</script>

<style lang="scss">
    .main-content{
        height: 100%;

        .banner-div {
            width: 90%;
            margin: auto;
            height: 10%;

            .question-title {
                margin: auto;
                display: flex;

                .question-p {
                    width: 30%;
                    text-align: center;
                    line-height: 40px;
                    background: white;
                }
                .question-button {
                    margin-left: 10%;
                }
            }
        }

        .content-div {
            width: 90%;
            height: 90%;
            margin: auto;
            display: flex;

            .left-question {
                width: 80%;
                border: 1px solid #fff;

                .select-drop-menu {
                    height: 10%;
                    background: #d3ebd5;

                    .plateform {
                        margin-right: 10%;
                    }

                    .width-20 {
                        width: 20%;
                    }
                    .float-right {
                        position: relative;
                        float: right;
                        line-height: 3rem;
                    }
                }

                .message-content {
                    margin-top: 1.5%;

                    .message-main {
                        overflow: hidden;
                        text-overflow: ellipsis;
                        display: -webkit-box;
                        -webkit-line-clamp: 2;
                        -webkit-box-orient: vertical;
                    }

                    .message-poster {
                        .margin-20 {
                            margin-left: 5%;
                            margin-right: 5%;
                        }
                        .background-green {
                            color: #11e13e;
                            margin-right: 5%;
                        }
                        .float-right{
                            position: relative;
                            float: right;
                            cursor: pointer;
                        }
                    }
                }
            }
            .right-difference {
                width: 20%;
                border: 1px solid #fff;

                .all-difference {
                    border: 1px solid #ccc;
                    box-shadow: 5px 5px 5px  #ffffff;
                }

                .hot-question {
                    margin-top: 10%;
                    border: 1px solid #ccc;
                    box-shadow: 5px 5px 5px  #ffffff;
                }
            }
        }

    }
</style>