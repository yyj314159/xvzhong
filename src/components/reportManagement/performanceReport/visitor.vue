<template>
    <div class="visitor">
        <Layout :style="{marginLeft: '200px'}" >
            <Content :style="{padding: '0 16px 16px'}" style="background:#fff;">
                <div id="top">
                    <div class="title"><span>筛选条件</span></div>
                    <div class="ipt">
                        <Select style="width:200px" placeholder="省">
                            <Option v-for="item in cityList" :value="item.value" :key="item.value">{{ item.label }}</Option>
                        </Select>
                        <Select style="width:200px" placeholder="市">
                            <Option v-for="item in cityList" :value="item.value" :key="item.value">{{ item.label }}</Option>
                        </Select>
                        <Select style="width:200px" placeholder="区">
                            <Option v-for="item in cityList" :value="item.value" :key="item.value">{{ item.label }}</Option>
                        </Select>
                        <Select style="width:200px" placeholder="项目名称">
                            <Option v-for="item in cityList" :value="item.value" :key="item.value">{{ item.label }}</Option>
                        </Select>
                        <Button type="success">搜索</Button>
                    </div>
                </div>
            </Content>
        </Layout>
    </div>
</template>

<script>
export default {
  name: 'Jiahua',
  data () {
    return {
       
  }
 }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped  lang="scss">
    #top{height: 100px;width: 100%;background:#fff;box-shadow: 0 1px 1px rgba(0,0,0,.1);border-radius:5px;overflow: hidden;}
    .title{width: 100%;height: 40px;background: #5BC0DE;line-height: 40px;color: #fff;}
    .ipt{width: 100%;height: 60px; display: flex;justify-content: space-around; align-items: center;}
</style>