<template>
  <div class="icon">
    <swiper>
      <swiper-slide v-for="(page,index) of pages" :key="index">
        <div class="child" v-for="item of page" :key="item.id">
          <div class="child-img">
            <img class="imgself" :src="item.imgurl" />
          </div>
          <p class="child-font">{{item.desc}}</p>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>
<script>
export default {
  name: 'icons',
  data () {
    return {
      swiperList: [
        {
          id: '1',
          imgurl: 'http://img0.imgtn.bdimg.com/it/u=2383721088,3169429672&fm=26&gp=0.jpg',
          desc: '热门景点1'
        },
        {
          id: '2',
          imgurl: 'http://img0.imgtn.bdimg.com/it/u=2383721088,3169429672&fm=26&gp=0.jpg',
          desc: '热门景点1'
        },
        {
          id: '3',
          imgurl: 'http://img0.imgtn.bdimg.com/it/u=2383721088,3169429672&fm=26&gp=0.jpg',
          desc: '热门景点1'
        },
        {
          id: '4',
          imgurl: 'http://img0.imgtn.bdimg.com/it/u=2383721088,3169429672&fm=26&gp=0.jpg',
          desc: '热门景点1'
        },
        {
          id: '5',
          imgurl: 'http://img0.imgtn.bdimg.com/it/u=2383721088,3169429672&fm=26&gp=0.jpg',
          desc: '热门景点1'
        },
        {
          id: '6',
          imgurl: 'http://img0.imgtn.bdimg.com/it/u=2383721088,3169429672&fm=26&gp=0.jpg',
          desc: '热门景点1'
        },
        {
          id: '7',
          imgurl: 'http://img0.imgtn.bdimg.com/it/u=2383721088,3169429672&fm=26&gp=0.jpg',
          desc: '热门景点1'
        },
        {
          id: '8',
          imgurl: 'http://img0.imgtn.bdimg.com/it/u=2383721088,3169429672&fm=26&gp=0.jpg',
          desc: '热门景点1'
        },
        {
          id: '9',
          imgurl: 'http://img0.imgtn.bdimg.com/it/u=2383721088,3169429672&fm=26&gp=0.jpg',
          desc: '热门景点1'
        }]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.swiperList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages(page)) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>
<style lang="stylus" scoped>
.icon {
  overflow: hidden;
  width: 100%;
  height: 0;
  padding-bottom: 50%;

  .child {
    position: relative;
    overflow: hidden;
    float: left;
    width: 25%;
    height: 0;
    padding-bottom: 25%;

    .child-img {
      position: absolute;
      left: 0;
      right: 0;
      top: 0;
      padding-bottom: 0.4rem;
      box-sizing: border-box;
      padding: 0.1rem;

      .imgself {
        display: block;
        margin: 0 auto;
        width: 70%;
      }
    }

    .child-font {
      position: absolute;
      left: 0;
      right: 0;
      bottom: 0;
      height: 0.4rem;
      line-height: 0.4rem;
      text-align: center;
    }
  }
}
</style>
