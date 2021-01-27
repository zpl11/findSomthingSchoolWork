<template>
    <div class="Home">
        <el-container>
            <el-header class="header-background">
                <school-header></school-header>
            </el-header>
            <el-main class="main-background">
                <main-content v-if="countIndex == 1"></main-content>
                <mainContent_02 v-if="countIndex == 2"></mainContent_02>
                <mainContent_03 v-if="countIndex == 3"></mainContent_03>
                <mainContent_04 v-if="countIndex == 4"></mainContent_04>
            </el-main>
            <el-footer class="foot-background">Footer</el-footer>
        </el-container>

    </div>
</template>

<script>
import schoolHeader from '../components/schoolHeader';
import mainContent from '../components/mainContent';
import mainContent_02 from '../components/mainContent_02';
import mainContent_03 from '../components/mainContent_03';
import mainContent_04 from '../components/mainContent_04';
export default {
    'name': 'Home',

    'components':{
        schoolHeader,
        mainContent,
        mainContent_02,
        mainContent_03,
        mainContent_04
    },

    'computed': {
        countIndex(){
            return this.$store.state.contentIndex;
        }
    },

    data(){
        return {

        };
    },

    'methods': {
        showContentIndex(contentIndex){
            this.showIndexContent = contentIndex;
        }
    },

    'watch': {

    }

};
</script>

<style lang="scss">
    .Home {
        color: #2b2b2b;

        .header-background {
            height: 10vh;
            background: #2c3e50;
        }

        .main-background {
            height: 80vh;
            background: #bbd8ff;
        }

        .foot-background {
            height: 10vh;
        }
    }
</style>