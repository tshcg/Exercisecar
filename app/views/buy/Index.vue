<template>
    <div>
        <Layout>
            <Sider hide-trigger :style="{background: '#fff'}">
                <Menu :active-name="$store.state.routerStore.col2ndname" theme="light" width="auto" @on-select="selectHandler">
                    <MenuItem name="carlist">精选车辆</MenuItem>
                    <MenuItem name="ai">推荐车辆</MenuItem>
                    <MenuItem name="sifa">更多</MenuItem>
                </Menu>
                
            </Sider>
            <Layout :style="{padding: '0 24px 24px'}">
                <Breadcrumb :style="{margin: '24px 0'}">
                    <BreadcrumbItem>首页</BreadcrumbItem>
                    <BreadcrumbItem>轿车求购</BreadcrumbItem>
                    <BreadcrumbItem>精选车辆</BreadcrumbItem>
                </Breadcrumb>
                <Content :style="{padding: '24px', minHeight: '280px', background: '#fff'}">
                    <router-view></router-view>
                </Content>
            </Layout>
        </Layout>
    </div>
</template>

<script>
    export default {
        methods : {
            //点击侧边栏的链接
            selectHandler(n){
                this.$router.push({"name" : n});
            }
        }
    }
</script>

<style scoped>

</style>