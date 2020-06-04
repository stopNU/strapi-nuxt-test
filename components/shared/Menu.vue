<template>
    <div class="outer-wrapper">
        <div class="inner-wrapper">
            <div class="content-wrapper">
                <el-menu
                    :default-active="activeIndex2"
                    class="el-menu"
                    mode="horizontal"
                    @select="handleSelect"
                    text-color="#FFFFFF"
                    background-color="transparent"
                    active-text-color="#ffd04b">
                    <el-menu-item index="1">Processing Center</el-menu-item>
                    <el-submenu index="2">
                        <template slot="title">Workspace</template>
                        <el-menu-item index="2-1">item one</el-menu-item>
                        <el-menu-item index="2-2">item two</el-menu-item>
                        <el-menu-item index="2-3">item three</el-menu-item>
                        <el-submenu index="2-4">
                        <template slot="title">item four</template>
                        <el-menu-item index="2-4-1">item one</el-menu-item>
                        <el-menu-item index="2-4-2">item two</el-menu-item>
                        <el-menu-item index="2-4-3">item three</el-menu-item>
                        </el-submenu>
                    </el-submenu>
                    <el-menu-item index="3"><a href="/about">About</a></el-menu-item>
                    <el-menu-item index="4"><a href="https://www.ele.me" target="_blank">Orders</a></el-menu-item>
                </el-menu>
            </div>
        </div>
    </div>
</template>

<script>
  export default {
    data() {
      return {
        activeIndex: '1',
        activeIndex2: '1'
      };
    },
    methods: {
      handleSelect(key, keyPath) {
        console.log(key, keyPath);
      }
    }
  }
</script>

<style scoped lang="scss">
    .outer-wrapper{
        background-color:rgba(1, 11, 27, 0.8);
        position: fixed;
        width: 100%;
        &.inner-wrapper, .content-wrapper{
            height: 115px;
        }
        .content-wrapper{
            display: flex;
            align-items: center;
        }
    }
    .el-menu{
        
    }
</style>