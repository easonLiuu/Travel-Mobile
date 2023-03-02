<template>
    <div >
        <div class="title">周末去哪儿</div>
        <ul>
            <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
                <div class="item-img-wrapper">
                    <img class="item-img" :src="item.imgUrl" alt="">
                </div>
                <div class="item-info">
                    <p class="item-title">{{item.title}}</p>
                    <p class="item-desc">{{item.desc}}</p>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1510/6e/1ea71e2f04e.jpg_r_640x214_aa6f091d.jpg',
        title: '故宫',
        desc: '东方宫殿建筑代表，世界宫殿建筑典范'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/aa/7baaf8a851d221.jpg_r_640x214_1431200f.jpg',
        title: '南山滑雪场',
        desc: '北京专业级滑雪圣地'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1501/f4/f467729126949c3a.water.jpg_140x140_ef235b1c.jpg',
        title: '天安门广场',
        desc: '我爱北京天安门，天安门上太阳升'
      }, {
        id: '0004',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1501/40/40b2b6c951b28fdd.water.jpg_140x140_1c863e5c.jpg',
        title: '水立方',
        desc: '中国的荣耀，阳光下的晶莹水滴'
      }, {
        id: '0005',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201308/23/b283071686e64dfec8d65eac.jpg_140x140_8c5a7c49.jpg',
        title: '温都水城养生馆',
        desc: '各种亚热带植物掩映其间仿佛置身热带雨林'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl'
.title
    margin-top: .2rem
    line-height: .8rem
    background: #eee
    text-indent: .2rem
.item-img-wrapper
    overflow: hidden
    height: 0
    padding-bottom: 33.9%
    .item-img
        width: 100%
.item-info
    padding: .1rem
    .item-title
        line-height: .54rem
        font-size: .32rem
        ellipsis()
    .item-desc
        line-height: .4rem
        color: #ccc
        ellipsis()
</style>
