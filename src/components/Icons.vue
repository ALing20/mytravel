<template>
  <div class="icons">
    <swiper :options="swiperOption">
      <swiper-slide v-for="(page, index) of pages" :key="index">
        <div
          class="icon"
          v-for="item of page"
          :key="item.id"
        >
          <div class='icon-img'>
            <img class='icon-img-content' :src='item.iconUrl' />
          </div>
          <p>{{item.content}}</p>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>
<script>
export default {
    name: 'HomeIcons',
    data () {
        return {
            swiperOption: {
                // 自动轮播
                autoplay:false,
            },
            IconList:[
                {
                    id: '0001',
                    iconUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
                    content:'热门景点'
                },
                {
                    id: '0002',
                    iconUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/e98eea7ed037b04a5af0250ca8a1abd7.png',
                    content:'少林寺'
                },
                {
                    id: '0003',
                    iconUrl: 'http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
                    content:'郑州必游'
                },
                {
                    id: '0004',
                    iconUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/8246f27355943202.png',
                    content:'郑州方特'
                },
                {
                    id: '0005',
                    iconUrl: 'http://img1.qunarzz.com/piao/fusion/1803/85/77241e9427222b02.png',
                    content:'郑州园博园'
                },
                {
                    id: '0006',
                    iconUrl: 'http://img1.qunarzz.com/piao/fusion/1803/b2/bfbc5d66e0ab5a02.png',
                    content:'冰雪世界'
                },
                {
                    id: '0007',
                    iconUrl: 'http://img1.qunarzz.com/piao/fusion/1803/fa/2548667cb6e902.png',
                    content:'郑州动物园'
                },
                {
                    id: '0008',
                    iconUrl: 'http://img1.qunarzz.com/piao/fusion/1803/e3/67df61427c8e1302.png',
                    content:'实景演出'
                },
                {
                    id: '0009',
                    iconUrl: 'http://img1.qunarzz.com/piao/fusion/1803/fa/2548667cb6e902.png',
                    content:'郑州动物园'
                },
                {
                    id: '0010',
                    iconUrl: 'http://img1.qunarzz.com/piao/fusion/1803/e3/67df61427c8e1302.png',
                    content:'实景演出'
                }
            ]
        }
    },
    computed: {
    pages () {
      const pages = []
      this.IconList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>
<style lang="less" scoped>
    @import '../assets/styles/varibles.less';
    .icons {
        height: 0;
        padding-bottom: 50%;
        margin-top: .1rem;
        .icon {
            position: relative;
            overflow: hidden;
            float: left;
            width: 25%;
            height: 0;
            padding-bottom: 25%;
            .icon-img {
                position: absolute;
                top: 0;        
                left: 0;
                right: 0;
                bottom: .44rem;
                box-sizing: border-box;
                padding: .1rem;
                .icon-img-content {
                    display: block;
                    margin: 0 auto;
                    height: 100%;
                }
             }
             p {
                position: absolute;
                left: 0;
                right: 0;
                bottom: 0;
                height: .44rem;
                line-height: .44rem;
                text-align: center;   
                // 文字太多就转成....显示
                overflow: hidden;
                white-space: nowrap;
                text-overflow: ellipsis;                           
            }
        }
    }
</style>
