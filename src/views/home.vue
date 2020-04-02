<template>
    <div class="home">
       <div v-for="(item,index) in diyComponents" :key="index">
           <diy-search :diyStyle="item" v-if="item.type=='search'"/>
       </div>
    </div>
</template>

<script>
import diySearch from '@/components/diySearch'
export default {
    data(){
        return {
            // pageType:1:系统页面-首页，2：系统页面-会员中心，3系统页面-商品详情页，应用：4分销中心，5积分商城，6整点秒杀，7兑换中心
            pageType: '',
            diyComponents: [
                {
                    type: 'search',
                    searchType: '1', // 搜索类型
                    warpBg: '#fff', // 搜素框外围背景
                    inputBg: '#999999', // 输入框背景
                    textStyle: { // 文字样式
                        color: '#fff',
                        textAlign: 'left'
                    },
                    iconColor: '#b4b4b4', // 图标颜色
                    searchText: '请输入关键字进行搜素', // 搜素的文字
                    paddingUd: 10, // 上下边距
                    paddingLr: 10, // 左右边距
                    borderRadius: '10' // 搜索框圆角
                },
            ]
        }
    },
    components: {
        diySearch
    },
    methods:{

    },
}
</script>
<style lang="scss" scoped>
  .home{
      width: 100%;
      height: 100%;
      /*padding: 0 10px;*/
  }
</style>
