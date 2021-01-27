<template>
    <div class="main-content">
        首页
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

    }
</style>