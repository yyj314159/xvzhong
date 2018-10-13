<template>
  <div id="app" class="layout">
    <!-- <img src="./assets/logo.png"> -->
    <Sider :style="{position: 'fixed', height: '100vh', left: 0, overflow: 'auto'}" style="background:#39435B">
            <Menu active-name="1-2" theme="dark" width="auto" :open-names="['1']" accordion style="background:#39435B">
               
               <div class="logo" >logo</div>

               

                
                    <Submenu name="1" >
                        <template slot="title">
                            <router-link to="./home" tag="span">
                                <Icon type="ios-compass" />
                                旭中首页
                            </router-link>
                        </template>
                        
                    </Submenu>
                
                
                <Submenu name="2" >
                    <template slot="title">
                        <Icon type="md-list-box" />
                        项目管理
                    </template>
                    <MenuItem name="2-1">添加醒目</MenuItem>
                    <MenuItem name="2-2">项目列表</MenuItem>
                    <MenuItem name="2-3">消息反馈</MenuItem>
                </Submenu>
               
                <Submenu name="3">
                    <template slot="title">
                        <Icon type="md-pricetags" />
                        调研对象管理
                    </template>
                    <MenuItem name="3-1">调研对象列表</MenuItem>
                    <MenuItem name="3-2">更新记录</MenuItem>
                </Submenu>
                <Submenu name="4">
                    <template slot="title">
                        <Icon type="md-checkbox-outline" />
                        审核管理
                    </template>
                    <MenuItem name="4-1">审核安排</MenuItem>
                    <MenuItem name="4-2">审核退回</MenuItem>
                    <MenuItem name="4-3">审核列表</MenuItem>
                </Submenu>
                <Submenu name="5">
                    <template slot="title">
                        <Icon type="md-pie" />
                        门店管理
                    </template>
                    <MenuItem name="5-1">添加门店</MenuItem>
                    <MenuItem name="5-2">门店列表</MenuItem>
                </Submenu>
                <Submenu name="6">
                    <template slot="title">                     
                            <Icon type="ios-cube" />
                            企业管理                       
                    </template>

                    
                       <MenuItem name="6-1" >
                          <router-link to="./moban" tag="span">模板管理</router-link>
                       </MenuItem>
                       <MenuItem name="6-2" >
                          <router-link to="./yuangong" tag="span">员工管理</router-link>
                       </MenuItem>
                    
                    
                    <MenuItem name="6-3">
                       <router-link to="./daili" tag="span">代理管理</router-link>
                    
                    </MenuItem>
                    <MenuItem name="6-4">
                        <router-link to="./fangwenyuan" tag="span">访问员管理</router-link>
                    </MenuItem>

                    <MenuItem name="6-5">
                       <router-link to="./quanxian" tag="span">权限管理</router-link>
                    </MenuItem>
                    <MenuItem name="6-6">
                        <router-link to="./dodata" tag="span">操作日志</router-link>
                    </MenuItem>
                </Submenu>
               <Submenu name="7">
                <template slot="title">
                    <Icon type="ios-create" />
                    报告管理
                </template>
                <MenuItem name="7-1">                  
                    <router-link to="./performanceReportVisitor" tag="span">业绩报告</router-link>                  
                    <!-- <MenuItem name="7-1-2">
                        <router-link to="./performanceReport/agent" tag="span">代理绩效</router-link>
                    </MenuItem>
                    <MenuItem name="7-1-3">
                        <router-link to="./performanceReport/examine" tag="span">审核绩效</router-link>
                    </MenuItem>                                  -->
                </MenuItem>
                <MenuItem name="7-2">
                    <router-link to="./reportTemplateList" tag="span">报告模板</router-link>
                </MenuItem>
                <MenuItem name="7-3">
                    <router-link to="./prescriptionReportList" tag="span">实效报告</router-link>
                </MenuItem>
                <MenuItem name="7-4">
                <router-link to="./familyReportList" tag="span"> 家化报告</router-link>
                </MenuItem>
                <MenuItem name="7-5">
                    <router-link to="./generatedReportList" tag="span">已生成报告</router-link>
                </MenuItem>               
            </Submenu>
                <Submenu name="8">
                    <template slot="title">
                        <Icon type="md-eye" />
                        可视化管理
                    </template>
                   
                </Submenu>
                <Submenu name="9">
                    <template slot="title">
                        <Icon type="ios-contact" />
                        我的任务
                    </template>
                    <MenuItem name="9-1">项目列表</MenuItem>
                    <MenuItem name="9-2">一审任务</MenuItem>
                    <MenuItem name="9-3">二审任务</MenuItem>
                    <MenuItem name="9-4">算分任务</MenuItem>
                    <MenuItem name="9-5">消息反馈</MenuItem>
                </Submenu>
            </Menu>
        </Sider>
        <Layout :style="{marginLeft: '200px'}" style="background:red">
            <Header :style="{background: '#fff', boxShadow: '0 2px 3px 2px rgba(0,0,0,.1)'}">
               <ul class="loader">
                  <li>【王茂如】</li>
                  <li>【项目经理】</li>
                  <li>【修改密码】</li>
                </ul>

            </Header>
            <!-- <Content :style="{padding: '0 16px 16px'}">
                <Breadcrumb :style="{margin: '16px 0'}">
                    <BreadcrumbItem>Home</BreadcrumbItem>
                    <BreadcrumbItem>Components</BreadcrumbItem>
                    <BreadcrumbItem>Layout</BreadcrumbItem>
                </Breadcrumb>
                <Card>
                    <div style="height: 600px">Content</div>
                </Card>
            </Content> -->
        </Layout>
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App',
  data(){
      return{
         
      }
  },
  methods:{
     aaa(){
         console.log("222")
        // this.$router.push("/home")
     }
  }
}
</script>
    
<style >
#app {
  
        /* body,ul,li,dl,dt,dd,p,ol,h1,h2,h3,h4,h5,h6,form,img,table,fieldset,legend,menu,input,button{
          margin:0;padding:0;
          }
        ul,li,ol{list-style:none;}
        img,fieldset{border:0; }
        img{display:block;}
        a{text-decoration:none; color:#333;}
        h1,h2,h3,h4,h5,h6{font-weight:500;}
        body{ font-family:"微软雅黑";}
        input,a{outline:none;} */
  
}


.layout{
        border: 1px solid #d7dde4;
        background: #f5f7f9;
        position: relative;
        border-radius: 4px;
        overflow: hidden;
    }
    .layout-header-bar{
        background: #fff;
        box-shadow: 0 1px 1px rgba(0,0,0,.1);
    }
  .logo{
     width: 200px;height: 40px;background:#293743
  }
   ul,li,ol{list-style:none;}

  .loader{float:right;
           width: 280px;
           height: 65px;
           font-weight: bold;
           font-size: 14px;
           display: flex;
           justify-content: space-around;

  }
  li {cursor: pointer;}

</style>
