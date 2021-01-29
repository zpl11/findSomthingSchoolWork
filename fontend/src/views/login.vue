<template>
    <div class="login">
        <div class="main-content">
            <div class="background-rectangle"></div>
            <div class="login-form">
                <div class="person-icon">
                    <img src="../assets/icon/人群.png" alt="" height="50" width="50">
                </div>
                <div class="form-title">
                    <p>石家庄学院生活服务平台</p>
                </div>
                <div class="form-login">
                    <el-input suffix-icon="el-icon-user" v-model="userName"></el-input>
                    <el-input suffix-icon="el-icon-view" v-model="password"></el-input>
                    <div class="wid-100">
                        <el-button type="primary" class="button-width">登录</el-button>
                    </div>
                    <p class="sign-in-word">还未注册?</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    "name": "login",
    data(){
        return {
            userName:'',
            password:''
        }
    }
};
</script>

<style lang="scss">
    .login {
        height: 100vh;
        width: 100vw;

        .el-input__inner {
            border-top: none;
            border-left: none;
            border-right: none;
        }

        .main-content{
            height: 100%;
            width: 100%;
            .background-rectangle {
                height: 20vh;
                width: 100%;
                position: absolute;
                top: 40vh;
                background: #1abc9c;
            }
            .login-form {
                width: 30%;
                height: 40%;
                border: 1px solid #cccccc;
                position: absolute;
                background: #ffffff;
                top: 30vh;
                left: 35vw;
                box-shadow: 2px 2px 2px 1px rgba(0, 0, 0, 0.2),
                -2px -2px 2px 1px rgba(0, 0, 0, 0.2),
                0px -4px 2px 0px #1abc9c;

                .person-icon {
                    height: 25%;
                    text-align: center;
                }
                .form-title {
                    text-align: center;
                    font-size: 1.3rem;
                    color: #1abc9c;
                    font-weight: 500;
                }
                .form-login {
                    .wid-100 {
                        width: 100%;
                        padding-left: 20%;
                        margin-top: 15px;
                        .button-width {
                            width: 60%;
                            margin: auto;
                        }
                    }
                    .sign-in-word {
                        text-align: center;
                        margin-top: 10px;
                        color: #1abc9c;
                        cursor: pointer;
                    }
                }
            }
        }
    }
</style>