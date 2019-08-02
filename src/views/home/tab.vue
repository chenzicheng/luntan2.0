<template>
  <div class="pc-home-tab1">
    <div class="content-warper clearfix">
      <div :class="{fixed:fixed}" class="nav">
        <div
          class="nav-item"
          :class="{'on':index==activeIndex}"
          @click="typeSelect(index)"
          v-for="(item,index) in typeList"
          :key="index"
        >{{item.typename}}</div>
      </div>
      <div class="pc-content clearfix">
        <div class="fl content-l">
          <div class="question-item" v-for="(item,index) in arr" :key="index">
            <div class="title clearfix">
              <span class="fl title-text">阿萨大大十大打撒阿斯顿</span>
              <span class="fr close">x</span>
            </div>
            <div
              class="text"
            >杂谈：我什么开始写博客，我又不是什么大犇？ 我写博客只是自己学习总结的一种方式 首先我很多遇见的问题都首先我很多遇见的问题都首先我很多遇见的问题都首先我很多遇见的问题都首先我很多遇见的问题都首先我很多遇见的问题都首先我很多遇见的问题都首先我很多遇见的问题都首先我很多遇见的问题都</div>
            <div class="user-info clearfix">
              <dl class="clearfix fl">
                <dd>
                  <img
                    src="https://statics.lotsmall.cn/image/20190420/20190420085850itoxef.jpeg?imageMogr2/thumbnail/640x/strip/quality/50"
                    alt
                  />
                </dd>
                <dd>
                  <span>asdad</span>
                </dd>
                <dd>asdadsa</dd>
                <dd>7天前</dd>
              </dl>
              <div class="fr num-info">
                <div class="fl num-detai reader-num">
                  <span class="text fl">阅读数</span>
                  <span class="num fl">111</span>
                </div>
                <div class="fl num-detai discuss-num">
                  <span class="text fl">评论数</span>
                  <span class="num fl">111</span>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="content-r fr">
          <div class="content-r-title clearfix">
            <span class="line"></span>
            <span class="txt">今日推荐</span>
          </div>
          <div class="right-box">
            <ul class="company-list">
              <li class="company-item clearfix">
                <div class="img-box">
                  <img
                    src="https://statics.lotsmall.cn/image/20190420/20190420085850itoxef.jpeg?imageMogr2/thumbnail/640x/strip/quality/50"
                    alt
                  />
                </div>
                <div
                  class="content"
                >爱仕达大所大所大大所大所大所大所大所大所大所大所大所爱仕达大所大所大大所大所大所大所大所大所大所大所大所爱仕达大所大所大大所大所大所大所大所大所大所大所大所</div>
              </li>
              <li class="company-item clearfix">
                <div class="img-box">
                  <img
                    src="https://statics.lotsmall.cn/image/20190420/20190420085850itoxef.jpeg?imageMogr2/thumbnail/640x/strip/quality/50"
                    alt
                  />
                </div>
                <div
                  class="content"
                >爱仕达大所大所大大所大所大所大所大所大所大所大所大所爱仕达大所大所大大所大所大所大所大所大所大所大所大所爱仕达大所大所大大所大所大所大所大所大所大所大所大所</div>
              </li>
              <li class="company-item clearfix">
                <div class="img-box">
                  <img
                    src="https://statics.lotsmall.cn/image/20190420/20190420085850itoxef.jpeg?imageMogr2/thumbnail/640x/strip/quality/50"
                    alt
                  />
                </div>
                <div
                  class="content"
                >爱仕达大所大所大大所大所大所大所大所大所大所大所大所爱仕达大所大所大大所大所大所大所大所大所大所大所大所爱仕达大所大所大大所大所大所大所大所大所大所大所大所</div>
              </li>
              <li class="company-item clearfix">
                <div class="img-box">
                  <img
                    src="https://statics.lotsmall.cn/image/20190420/20190420085850itoxef.jpeg?imageMogr2/thumbnail/640x/strip/quality/50"
                    alt
                  />
                </div>
                <div
                  class="content"
                >爱仕达大所大所大大所大所大所大所大所大所大所大所大所爱仕达大所大所大大所大所大所大所大所大所大所大所大所爱仕达大所大所大大所大所大所大所大所大所大所大所大所</div>
              </li>
              <li class="company-item clearfix">
                <div class="img-box">
                  <img
                    src="https://statics.lotsmall.cn/image/20190420/20190420085850itoxef.jpeg?imageMogr2/thumbnail/640x/strip/quality/50"
                    alt
                  />
                </div>
                <div
                  class="content"
                >爱仕达大所大所大大所大所大所大所大所大所大所大所大所爱仕达大所大所大大所大所大所大所大所大所大所大所大所爱仕达大所大所大大所大所大所大所大所大所大所大所大所</div>
              </li>
              <li class="company-item clearfix">
                <div class="img-box">
                  <img
                    src="https://statics.lotsmall.cn/image/20190420/20190420085850itoxef.jpeg?imageMogr2/thumbnail/640x/strip/quality/50"
                    alt
                  />
                </div>
                <div
                  class="content"
                >爱仕达大所大所大大所大所大所大所大所大所大所大所大所爱仕达大所大所大大所大所大所大所大所大所大所大所大所爱仕达大所大所大大所大所大所大所大所大所大所大所大所</div>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      activeIndex: 0,
      typeList: [
        {
          type: 'type1',
          typename: '类型1'
        },
        {
          type: 'type1',
          typename: '类型1类型1'
        },
        {
          type: 'type1',
          typename: '类型1'
        },
        {
          type: 'type1',
          typename: '类型1类型1'
        },
        {
          type: 'type1',
          typename: '类型1'
        },
        {
          type: 'type1',
          typename: '类型1'
        }
      ],
      fixed: false,
      arr: [1, 2, 3, 4, 5, 6, 7, 78, 8, 9, 90, 0, 0, 0]
    }
  },
  methods: {
    typeSelect(index) {
      // alert(1)
      // console.log('zz')
      // if (document.body) {
      //   document.body.scrollTop = 0
      // } else if (document.documentElement) {
      //   document.documentElement.scrollTop = 0
      // }
      this.activeIndex = index
      document.documentElement.scrollTop = 0
      document.body.scrollTop = 0
      this.arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 0, 0]
    }
  },
  mounted() {
    let _this = this
    function getScrollTop() {
      var scrollTop = 0,
        bodyScrollTop = 0,
        documentScrollTop = 0
      if (document.body) {
        bodyScrollTop = document.body.scrollTop
      }
      if (document.documentElement) {
        documentScrollTop = document.documentElement.scrollTop
      }
      scrollTop = bodyScrollTop - documentScrollTop > 0 ? bodyScrollTop : documentScrollTop
      console.log(scrollTop)
      if (scrollTop >= 40) {
        _this.fixed = true
      } else {
        _this.fixed = false
      }
      return scrollTop
    }

    //文档的总高度

    function getScrollHeight() {
      var scrollHeight = 0,
        bodyScrollHeight = 0,
        documentScrollHeight = 0
      if (document.body) {
        bodyScrollHeight = document.body.scrollHeight
      }
      if (document.documentElement) {
        documentScrollHeight = document.documentElement.scrollHeight
      }
      scrollHeight = bodyScrollHeight - documentScrollHeight > 0 ? bodyScrollHeight : documentScrollHeight
      return scrollHeight
    }

    //浏览器视口的高度

    function getWindowHeight() {
      var windowHeight = 0
      if (document.compatMode == 'CSS1Compat') {
        windowHeight = document.documentElement.clientHeight
      } else {
        windowHeight = document.body.clientHeight
      }
      return windowHeight
    }

    window.onscroll = function() {
      if (getScrollTop() + getWindowHeight() == getScrollHeight()) {
        _this.arr = _this.arr.concat([1, 2, 3, 4, 5, 6, 76, 7, 8, 9])
      }
    }
  }
}
</script>
<style lang="scss">
.pc-home-tab1 {
  background: #f5f6f7;
  .pc-content {
    .content-l {
      width: 760px;
      min-height: 500px;
      margin-right: 12px;
      .question-item {
        background: #fff;
        padding: 5px 15px;
        margin-bottom: 2px;
        &:hover {
          background: #fafafa;
        }
        .user-info {
          .num-info {
            .reader-num {
              padding-right: 5px;
              position: relative;
              &::after {
                position: absolute;
                content: '';
                height: 15px;
                width: 1px;
                top: 4px;
                right: 0;
                background: #e0e0e0;
              }
            }
            .discuss-num {
              margin-left: 5px;
            }
            .num-detai {
              .text {
                color: #8a8a8a;
                margin-right: 6px;
              }
              .num {
                color: #3399ea;
              }
              &:hover {
                .text {
                  color: #3399ea;
                }
              }
            }
          }
          dl {
            padding: 0;
            margin: 0;
            dd {
              float: left;
              padding: 0 7px;
              position: relative;
              &::after {
                position: absolute;
                content: '';
                height: 15px;
                width: 1px;
                background: #e0e0e0;
                top: 4px;
                right: 0;
              }
              img {
                height: 24px;
                width: 24px;
                border-radius: 50%;
              }
            }
          }
        }
        .text {
          margin-bottom: 4px;
          color: #8a8a8a;
          font-size: 14px;
          line-height: 24px;
          word-break: break-all;
          display: -webkit-box;
          -webkit-line-clamp: 1;
          /* ! autoprefixer: off */
          -webkit-box-orient: vertical;
          overflow: hidden;
        }
        .title {
          &:hover {
            .title-text {
              color: #cf2730;
            }
          }
          .title-text {
            color: #3d3d3d;
            font-size: 18px;
            font-weight: 600;
          }
          .close {
            font-size: 16px;
            cursor: pointer;
          }
        }
      }
    }
    .content-r {
      width: 300px;
      display: block;
      box-shadow: 0 1px 2px 0 rgba(0, 0, 0, 0.04);
      background: #fff;
      padding: 16px 16px;
      margin-bottom: 12px;
      margin-top: 0;
      .content-r-title {
        margin-bottom: 16px;
        .txt {
          display: block;
          float: left;
          font-size: 16px;
          color: #2c3033;
        }
        .line {
          float: left;
          width: 3px;
          height: 16px;
          background: #cf2730;
          overflow: hidden;
          margin-right: 5px;
          margin-top: 5px;
        }
      }
      .right-box {
        .company-list {
          list-style: none;
          margin: 0;
          padding: 0;
          .company-item {
            margin-bottom: 16px;
            &:hover {
              .content {
                color: #cf2730;
              }
            }
            &:last-child {
              margin-bottom: 0;
            }
            .img-box {
              float: left;
              padding-right: 10px;
              img {
                height: 48px;
                width: 64px;
                border-radius: 6px;
              }
            }
            .content {
              padding-top: 2px;
              word-break: break-all;
              display: -webkit-box;
              -webkit-line-clamp: 2;
              /* ! autoprefixer: off */
              -webkit-box-orient: vertical;
              overflow: hidden;
              font-weight: 600;
              margin-bottom: 3px;
              font-size: 14px;
              color: #3d3d3d;
              cursor: pointer;
            }
          }
        }
      }
    }
  }
  .content-warper {
    width: 1180px;
    padding: 12px 0 0;
    margin: 0 auto;
    .nav {
      float: left;
      width: 96px;
      background-color: #fff;
      margin-right: 12px;
      text-align: center;
      line-height: 32px;
      position: relative;
      padding: 6px 0;
      -webkit-box-shadow: 0 1px 2px 0 rgba(0, 0, 0, 0.04);
      box-shadow: 0 1px 2px 0 rgba(0, 0, 0, 0.04);
      &.fixed {
        position: fixed;
        top: 0;
      }
      .nav-item {
        border-bottom: 1px solid #fff;
        &:hover {
          background: #f44444;
          color: #fff;
        }
        &:last-child {
          border: none;
        }
        &.on {
          background: #f44444;
          color: #fff;
        }
      }
    }
    .pc-content {
      width: 1072px;
      float: right;
    }
  }
}
</style>
