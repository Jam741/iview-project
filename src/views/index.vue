<style scoped>
    .layout {
        border: 1px solid #d7dde4;
        background: #f5f7f9;
        position: relative;
        border-radius: 4px;
        overflow: hidden;
    }

    .layout-header-bar {
        background: #fff;
        box-shadow: 0 1px 1px rgba(0, 0, 0, .1);
    }
</style>
<template>
    <div class="layout">
        <Sider :style="{position: 'fixed', height: '100vh', left: 0, overflow: 'auto'}">
            <Menu active-name="1-2" theme="dark" width="auto" :accordion='true' :open-names="['1']"  @on-select="onMenuSelect" @on-open-change="onMenuOpenChange">

                <Submenu  name="1">
                    <template slot="title">
                        <Icon type="ios-navigate"></Icon>
                        保险公司管理
                    </template>
                    <MenuItem name="1-1" >保险公司列表</MenuItem>
                    <MenuItem name="1-2">Option 2</MenuItem>
                    <!--<MenuItem name="1-3">Option 3</MenuItem>-->
                </Submenu>
                <Submenu name="2">
                    <template slot="title">
                        <Icon type="ios-people"></Icon>
                        用户管理
                    </template>
                    <MenuItem name="2-1">用户列表</MenuItem>
                    <!--<MenuItem name="2-2">Option 2</MenuItem>-->
                </Submenu>
                <Submenu name="3">
                    <template slot="title">
                        <Icon type="ios-analytics"></Icon>
                        拼团管理
                    </template>
                    <MenuItem name="3-1">拼团列表</MenuItem>
                    <!--<MenuItem name="3-2">Option 2</MenuItem>-->
                </Submenu>
            </Menu>
        </Sider>
        <Layout :style="{marginLeft: '200px'}">
            <Header :style="{background: '#fff', boxShadow: '0 2px 3px 2px rgba(0,0,0,.1)'}">Car In</Header>
            <Content :style="{padding: '0 16px 16px'}">
                <Breadcrumb :style="{margin: '16px 0'}">
                    <BreadcrumbItem>Home</BreadcrumbItem>
                    <BreadcrumbItem>Components</BreadcrumbItem>
                    <BreadcrumbItem>Layout</BreadcrumbItem>
                </Breadcrumb>
                <Card>
                    <div style="height: 600px">Content</div>
                </Card>
            </Content>
        </Layout>
    </div>
</template>
<script>
    export default {
        data() {
            return {
                optionData: [
                    {
                        id: 1,
                        title: '保险公司管理',
                        childs: [
                            {
                                id :1-1,
                                title:'公司列表'
                            }
                        ]
                    },
                    {
                        id: 2,
                        title: '用户管理',
                        childs: [
                            {
                                id :2-1,
                                title:'用户列表'
                            }
                        ]
                    }
                ]
            }
        },
        mounted() {

        },
        beforeDestroy() {

        },
        methods: {
            onMenuSelect :function (e) {
                console.log(e)
            },

            onMenuOpenChange:function (e) {
                console.log(e)
            }
        }
    }
</script>