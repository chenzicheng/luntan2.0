<template>
  <div class="user-blog">
    <div class="blog-content">
      <div class="main">
        <div @click="go" v-for="(item,index) in 15" :key="index" class="item">
          <div class="title clearfix">
            <img
              class="fl"
              src="https://statics.lotsmall.cn/image/20190420/20190420085850itoxef.jpeg?imageMogr2/thumbnail/640x/strip/quality/50"
              alt
            />
            <h3 class="fl">奥术大师多撒奥多撒多撒大</h3>
          </div>
          <div
            class="intr"
          >CSDN已经坚持两年了，是时候祭出我的微信公众号了，当然我这个公众号是新申请的，里面消息还不是很多，但是我会经常更新，我的原则就是，绝不做死尸，绝不会像死尸一样躺在大家的手机里，占用大家手机的空间，当然了，CSDN也不会断，有些小伙伴就喜欢看CSDN，有些小伙伴就喜欢看微信公众号，所以我！CSDN已经坚持两年了，是时候祭出我的微信公众号了，当然我这个公众号是新申请的，里面消息还不是很多，但是我会经常更新，我的原则就是，绝不做死尸，绝不会像死尸一样躺在大家的手机里，占用大家手机的空间，当然了，CSDN也不会断，有些小伙伴就喜欢看CSDN，有些小伙伴就喜欢看微信公众号，所以我！</div>
          <div class="info clearfix">
            <div class="fl bar time">2019-07-08 15:10:22</div>
            <div class="fl bar">
              <span>阅读数</span>
              <span class="num">33</span>
            </div>
            <div class="fl bar">
              <span>评论数</span>
              <span class="num">0</span>
            </div>
            <div class="handle fr">
              <a-button class="edit" size="small">编辑</a-button>
              <a-button size="small" @click="showConfirm" type="danger">删除</a-button>
            </div>
          </div>
        </div>
      </div>
      <div class="footer">
        <a-pagination @change="pageChange" v-model="current" :total="500" />
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      current: 1
    }
  },
  methods: {
    go() {
      this.$router.push('/home/detail?id=1231asda')
    },
    showConfirm() {
      this.$confirm({
        title: '提示',
        content: '确认删除吗？',
        onOk() {
          //   return new Promise((resolve, reject) => {
          //     setTimeout(Math.random() > 0.5 ? resolve : reject, 1000)
          //   }).catch(() => console.log('Oops errors!'))
        },
        onCancel() {}
      })
    },
    pageChange(page) {
      console.log(page)
    }
  }
}
</script>
<style lang="scss">
.user-blog {
  background: #f5f6f7;
  padding-bottom: 20px;
  .blog-content {
    padding-top: 15px;
    width: 1200px;
    margin: 0 auto;
    .footer {
      margin-top: 10px;
    }
    .mian {
      box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.05);
    }
    .item {
      background: #fff;
      padding: 12px 24px;
      margin-bottom: 1px;
      &:last-child {
        margin-bottom: 0;
      }
      &:hover {
        background: #f5f6f7;
        .handle {
          display: inline-block;
        }
      }
      .handle {
        display: none;
        .edit {
          margin-right: 10px;
        }
      }
      .info {
        margin-top: 8px;
        .time {
          color: #6b6b6b;
        }
        .bar {
          position: relative;
          padding: 0 8px;
          &::before {
            position: absolute;
            content: '';
            height: 15px;
            width: 1px;
            background: #e0e0e0;
            top: 4px;
            right: 0;
          }
          .num {
            margin-left: 5px;
            color: #3399ea;
          }
          &:first-child {
            padding-left: 0;
          }
          &:last-child {
            &::before {
              width: 0;
            }
          }
        }
      }
      .intr {
        font-size: 14px;
        line-height: 22px;
        white-space: normal;
        color: #999;
        word-break: break-all;
        display: -webkit-box;
        -webkit-line-clamp: 2;
        /* ! autoprefixer: off */
        -webkit-box-orient: vertical;
        overflow: hidden;
      }
      .title {
        padding: 5px 0px;
        img {
          height: 28px;
          width: 28px;
          border-radius: 50%;
          margin-right: 5px;
        }
      }
    }
  }
}
</style>