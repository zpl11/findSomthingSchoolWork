<template>
    <div class="school-header">
        <div class="header-content">
            <el-row :gutter="10">
                <el-col :xs="4" :sm="4" :md="4" :lg="4" :xl="4">
                    <el-menu :default-active="activeIndex" class="el-menu-demo" mode="horizontal" background-color="#2c3e50">
                        <el-menu-item class="logo-color" index="0">石家庄学院失物招领平台</el-menu-item>
                    </el-menu>
                </el-col>
                <el-col :xs="16" :sm="16" :md="16" :lg="16" :xl="16">
                    <el-menu :default-active="activeIndex" class="el-menu-demo menu-center" mode="horizontal" @select="handleSelect" background-color="#2c3e50" active-text-color="#ffd04b">
                        <el-menu-item index="1">首页</el-menu-item>
                        <el-menu-item index="2">问题咨询</el-menu-item>
                        <el-menu-item index="3">失物招领</el-menu-item>
                        <el-menu-item index="4">心情话板</el-menu-item>
                    </el-menu>
                </el-col>
                <el-col :xs="4" :sm="4" :md="4" :lg="4" :xl="4">
                    <div class="grid-content bg-purple-light">
                        <el-menu :default-active="activeIndex" class="el-menu-demo" mode="horizontal" @select="userSelect" background-color="#2c3e50">
                            <el-submenu index="1">
                                <template slot="title">
                                    <span>
                                        <img src="../assets/icon/头像.svg" width="20">
                                    </span>
                                </template>
                                <el-menu-item index="2-1">我的主页</el-menu-item>
                                <el-menu-item index="2-2">我的消息</el-menu-item>
                                <el-menu-item index="2-3">个人设置</el-menu-item>
                                <el-menu-item index="2-3">退出</el-menu-item>
                            </el-submenu>
                        </el-menu>
                    </div>
                </el-col>

            </el-row>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'schoolHeader',

        data() {
            return {
                activeIndex: '1',
            };
        },
        methods: {
            // 切换下面的主体部分
            handleSelect(key, keyPath) {
                console.log(key, keyPath);
                this.$store.state.contentIndex = key;
            },
            // 个人登录选项
            userSelect(key, keyPath) {
                console.log(key, keyPath);
            }
        }
    };
</script>

<style lang="scss">
    .school-header {
        .header-content {
            /*消除 nav 导航底部白边*/
            .el-menu.el-menu--horizontal {
                border-bottom: none;
            }

            .logo-color {
                color: #11ff00;
            }
            .menu-center {
                text-align: center;
            }
        }
    }
</style>