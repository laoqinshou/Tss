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
          desc: '热门景点1热门景点1热门景点1热门景点1热门景点1'
        },
        {
          id: '2',
          imgurl: 'http://img0.imgtn.bdimg.com/it/u=2383721088,3169429672&fm=26&gp=0.jpg',
          desc: '热门景点2'
        },
        {
          id: '3',
          imgurl: 'http://img0.imgtn.bdimg.com/it/u=2383721088,3169429672&fm=26&gp=0.jpg',
          desc: '热门景点3'
        },
        {
          id: '4',
          imgurl: 'http://img0.imgtn.bdimg.com/it/u=2383721088,3169429672&fm=26&gp=0.jpg',
          desc: '热门景点4'
        },
        {
          id: '5',
          imgurl: 'http://img0.imgtn.bdimg.com/it/u=2383721088,3169429672&fm=26&gp=0.jpg',
          desc: '热门景点5'
        },
        {
          id: '6',
          imgurl: 'http://img0.imgtn.bdimg.com/it/u=2383721088,3169429672&fm=26&gp=0.jpg',
          desc: '热门景点6'
        },
        {
          id: '7',
          imgurl: 'http://img0.imgtn.bdimg.com/it/u=2383721088,3169429672&fm=26&gp=0.jpg',
          desc: '热门景点7'
        },
        {
          id: '8',
          imgurl: 'http://img0.imgtn.bdimg.com/it/u=2383721088,3169429672&fm=26&gp=0.jpg',
          desc: '热门景点8'
        },
        {
          id: '9',
          imgurl: 'http://img0.imgtn.bdimg.com/it/u=2383721088,3169429672&fm=26&gp=0.jpg',
          desc: '热门景点9'
        }]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.swiperList.forEach((item, index) => {
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
<style lang="stylus" scoped>
.icon {
  overflow: hidden;
  width: 100%;
  height: 0;
  padding-bottom: 50%;
<<<<<<< HEAD

=======
>>>>>>> origin/index-icons
  .child {
    position: relative;
    overflow: hidden;
    float: left;
    width: 25%;
    height: 0;
    padding-bottom: 25%;
<<<<<<< HEAD

=======
>>>>>>> origin/index-icons
    .child-img {
      position: absolute;
      left: 0;
      right: 0;
      top: 0;
      padding-bottom: 0.4rem;
      box-sizing: border-box;
      padding: 0.1rem;
<<<<<<< HEAD

=======
>>>>>>> origin/index-icons
      .imgself {
        display: block;
        margin: 0 auto;
        width: 70%;
      }
    }
<<<<<<< HEAD

=======
>>>>>>> origin/index-icons
    .child-font {
      position: absolute;
      left: 0;
      right: 0;
      bottom: 0;
      height: 0.4rem;
      line-height: 0.4rem;
      text-align: center;
      overflow hidden;
      white-space nowrap;
      text-overflow ellipsis;
    }
  }
}
<<<<<<< HEAD
</style>
=======
</style>
>>>>>>> origin/index-icons
