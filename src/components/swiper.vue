<template>
    <div class="wrapper">
        <swiper :options="swiperOption" v-if="swiperList.length">
            <swiper-slide v-for="item of swiperList" :key="item.id">
                <img class="swiper-img" :src="item.imgUrl" alt="">
            </swiper-slide>
            <div class="swiper-pagination"  slot="pagination"></div>
        </swiper>
    </div>
</template>

<script>
export default {
    name: 'HomeSwiper',
    data () {
        return{
            swiperOption: {
                pagination: '.swiper-pagination',
                // 让插件支持循环轮播
                loop: true,
                // 自动轮播
                autoplay:true,
                speed: 900,  // 切换图片速度
            },
            swiperList:[
                { 
                    id: '001',
                    imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/17e2352b857f66e9d2948e98dc483bc2.jpg_750x200_2857d0a3.jpg'
                },
                {
                    id: '002',
                    imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/33941bbe8d3921f7b7089f07187b5442.jpg_750x200_947ed0f6.jpg'
                },
                {
                    id: '003',
                    imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/e5104d77fbfdb522bd4fe4f0451e517f.jpg_750x200_7d44f64b.jpg'
                },
                {
                    id: '004',
                    imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/7a2314caa82d064842768e92cdf72255.jpg_750x200_7e586aee.jpg'
                },
                {
                    id: '005',
                    imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/a9658b2ee2c2c6de227c9710a8b04d48.jpg_750x200_f38fba28.jpg'
                }
            ]
        }
    }
}
</script>

<style lang="less" scoped>
    .wrapper /deep/ .swiper-pagination-bullet-active {
            background-color: #fff !important;
        }
    .wrapper {
        // // 为了使轮播图下面的内容在正常位置显示，而没有因为图片未加载完，底下内容有跳动上去的感觉
        // overflow: hidden;
        // width: 100%;
        // height: 0;
        // padding-bottom: 37.5%;
        .swiper-img {
            width: 100%;
        }
    }
</style>
