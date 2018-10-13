<template>
  <div class="hello">
     <Layout :style="{marginLeft: '200px'}">
            <tabs :animated="false">

                <!-- 产品模板 -->
                <tab-pane label="产品模板">
                    <Content :style="{padding: '0 16px 16px'}">
                        
                        <Card>
                            <div style="height: 600px">
                                <div class="sou">
                                    项目调查产品类别&nbsp;&nbsp;&nbsp;
                                    <el-select v-model="value8" filterable placeholder="请选择" style="width:280px">
                                        <el-option
                                        v-for="item in options"
                                        :key="item.value"
                                        :label="item.label"
                                        :value="item.value">
                                        </el-option>
                                    </el-select>
                                    &nbsp;&nbsp;
                                    <el-button type="success" >搜索</el-button>
                                    <el-button type="success">产品类别管理</el-button>
                                </div>
                                <!-- 表格 -->
                                <el-table
                                    :data="canpin"
                                    border
                                    style="width: 100%;"
                                    >
                                    <el-table-column
                                    prop="date"
                                    label=""
                                    width="180">
                                    </el-table-column>
                                    <el-table-column
                                    prop="name"
                                    label="名称"
                                    width="180">
                                    </el-table-column>
                                    <el-table-column
                                    prop="address"
                                    label="编号">
                                    </el-table-column>
                                     <el-table-column
                                    prop="tiaoxingma"
                                    label="条形码">
                                    </el-table-column>
                                     <el-table-column
                                    prop="price"
                                    label="是否需要价格">
                                    </el-table-column>
                                    <el-table-column
                                    prop="sort"
                                    label="排序">
                                    </el-table-column>
                                    <el-table-column
                                    prop="do"
                                    label="操作/添加父类">
                                    </el-table-column>
                                </el-table>
                            </div>
                        </Card>
                    </Content>
                </tab-pane>

                <!-- app项目模板 -->
                <tab-pane label="app项目模板">
                    <Content :style="{padding: '0 16px 16px'}">
                        
                        <Card>
                            <div style="height: 600px">
                                <div class="sou">
                                    项目类型&nbsp;&nbsp;&nbsp;
                                    <el-select v-model="value8" filterable placeholder="请选择" style="width:280px">
                                        <el-option
                                        v-for="item in options2"
                                        :key="item.value"
                                        :label="item.label"
                                        :value="item.value">
                                        </el-option>
                                    </el-select>
                                    &nbsp;&nbsp;
                                    <el-button type="success" >搜索</el-button>
                                    <el-button type="success" @click="tobianji">添加模板</el-button>
                                    <!-- <router-link to="/moban/bianji" ><el-button type="success" >添加模板</el-button></router-link> -->
                                    
                                </div>
                                <!-- 表格 -->
                                <el-table
                                    :data="app"
                                    border
                                    style="width: 100%;"
                                    >
                                    <el-table-column
                                    prop="type"
                                    label="项目类型"
                                    width="180">
                                    </el-table-column>
                                    <el-table-column
                                    prop="title"
                                    label="模板名称"
                                    width="180">
                                    </el-table-column>
                                    <el-table-column
                                    prop="miaoshu"
                                    label="备注描述">
                                    </el-table-column>
                                     <el-table-column
                                    prop="caozuo"
                                    label="操作">
                                    </el-table-column>
                                     
                                </el-table>
                            </div>
                        </Card>
                    </Content>
                </tab-pane>


                <!-- 算分模板 -->
                <tab-pane label="算分模板">
                    <Content :style="{padding: '0 16px 16px'}">
                        
                        <Card>
                            <div style="height: 600px">
                                <div style="height: 600px">
                                    <div class="sou">
                                        项目类型&nbsp;&nbsp;&nbsp;
                                        <el-select v-model="value8" filterable placeholder="请选择" style="width:280px">
                                            <el-option
                                            v-for="item in options3"
                                            :key="item.value"
                                            :label="item.label"
                                            :value="item.value">
                                            </el-option>
                                        </el-select>
                                        &nbsp;&nbsp;
                                        <el-button type="success" >搜索</el-button>
                                        <el-button type="success" @click="tonew">添加模板</el-button>
                                    </div>
                                    <!-- 表格 -->
                                    <el-table
                                        :data="suanfa"
                                        border
                                        style="width: 100%;"
                                        >
                                        <el-table-column
                                        prop="type"
                                        label="项目类型"
                                        width="180">
                                        </el-table-column>
                                        <el-table-column
                                        prop="title"
                                        label="模板名称"
                                        width="180">
                                        </el-table-column>
                                        <el-table-column
                                        prop="miaoshu"
                                        label="备注描述">
                                        </el-table-column>
                                        <el-table-column
                                        prop="caozuo"
                                        label="操作">
                                        </el-table-column>
                                        
                                    </el-table>
                                </div>
                            </div>
                        </Card>
                    </Content>
                </tab-pane>
            </tabs>
            
            
        </Layout>
    
  </div> 
</template>

<script>
export default {
  name: 'Moban',
//   methods: {
//       tableRowClassName({row, rowIndex}) {
//         if (rowIndex === 1) {
//           return 'warning-row';
//         } else if (rowIndex === 3) {
//           return 'success-row';
//         }
//         return '';
//       }
//     },

  data () {
    return {
        //111
        options: [{
          value: '选项1',
          label: '黄金糕'
        }, {
          value: '选项2',
          label: '双皮奶'
        }, {
          value: '选项3',
          label: '蚵仔煎'
        }, {
          value: '选项4',
          label: '龙须面'
        }, {
          value: '选项5',
          label: '北京烤鸭'
        }],
        //222
        options2: [{
          value: '选项1',
          label: '实化'
        }, {
          value: '选项2',
          label: '家化'
        }, {
          value: '选项3',
          label: '问卷'
        }],
        //333
        options3: [{
          value: '选项1',
          label: '111'
        }, {
          value: '选项2',
          label: '222'
        }, {
          value: '选项3',
          label: '333'
        }],




        value8: '',

        //表格
        //111
        canpin: [{
          date: '2016-05-02',
          name: '王小虎',
          address: '222',
          tiaoxingma:"222",
          price:"555",
          sort:"0",
          do:56
        }, {
          date: '2016-05-02',
          name: '王小虎',
          address: '88888888888888',
          tiaoxingma:"222",
          price:"555",
          sort:"0",
           do:56
        }],

        // 222
        app: [{
          type: '2016-05-02',
          title: '但vs方法是拜拜',
          miaoshu: '496288+65656',
          caozuo:"编辑",
          
        }],
        //333
        suanfa: [{
          type: 'adfdafdfd',
          title: 'ggggggggg',
          miaoshu: 'ggggg+65656',
          caozuo:"编辑",
          
        }],



      }
  },
  methods:{
    tobianji(){
      this.$router.push("/bianji")
    },
    tonew(){
      this.$router.push("/new")

    }
    // addnew(){
    //     this.$router.push("/chalan_jia")
    // }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped  lang="scss">
    .sou{
        width: 100%;height: 50px;display: flex;align-items: center;margin-bottom: 25px
    }
.el-table .warning-row {
    background: oldlace;
  }

  .el-table .success-row {
    background: #f0f9eb;
  }
</style>
