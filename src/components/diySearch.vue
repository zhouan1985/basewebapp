<template>
    <van-search
         ref="vansearch"
        :background="diyStyle.warpBg"
        :input-align="diyStyle.textStyle.textAlign"
        :placeholder="diyStyle.searchText"
        :shape="diyStyle.borderRadius == '0' ? 'square' : 'round'"
        v-model="value"
    />
</template>

<script>
    export default {
        name: "diySearch",
        props:{
            diyStyle:{
                type: Object,
                default: null
            }
        },
        data() {
            return {
                value: ''
            }
        },
        mounted(){
           console.log(this.$refs.vansearch)
        }
    }
</script>

<style scoped>

</style>
