<template>
    <div class="about">
        <el-container>
            <el-header>Header</el-header>
            <el-container>
                <el-aside width="200px">
                    <el-row class="tac">
                        <el-col :span="12">
                            <el-menu
                                    :default-active="$route.path"
                                    @close="handleClose"
                                    @open="handleOpen"
                                    class="el-menu-vertical-demo"
                                    router>
                                <el-submenu index="/">
                                    <template slot="title">
                                        <i class="el-icon-location"></i>
                                        <span>测试demo</span>
                                    </template>
                                    <el-menu-item-group index>
                                        <el-menu-item index="/frame/colorTest">颜色测试</el-menu-item>
                                    </el-menu-item-group>
                                    <el-menu-item-group index>
                                        <el-menu-item index="/frame/HelloWorld">HelloWord</el-menu-item>
                                    </el-menu-item-group>
                                    <el-menu-item-group index>
                                        <el-menu-item index="/frame/chartTest">chartTest</el-menu-item>
                                    </el-menu-item-group>
                                </el-submenu>
                            </el-menu>
                        </el-col>
                    </el-row>

                </el-aside>
                <el-main>
                    <router-view></router-view>
                </el-main>
            </el-container>
        </el-container>
    </div>
</template>
<script>
    export default {
        data() {
            return {}
        },
        methods: {
            handleOpen(key, keyPath) {
                console.log(key, keyPath);
            },
            handleClose(key, keyPath) {
                console.log(key, keyPath);
            }
        },
        created() {
            console.log(this.$router)
        },
    }
</script>
<style lang="scss" scoped>
    @import "../assets/ThemeStyle/theme.scss";
    .el-header{
        background-color: $colorHead;
        color: #333;
        text-align: center;
    }

    .el-aside {
        background-color: $colorAside;
        color: #333;
        text-align: center;
    }

    .el-main {
        background-color: $colorMain;
        color: #333;
        text-align: center;
    }

</style>
