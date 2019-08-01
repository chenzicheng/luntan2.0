<template>
  <div class="pc-home">
    <div class="pc-header clearfix">
      <div class="box">
        <ul class="clearfix">
          <li>
            <img
              class="logo-img"
              src="https://statics.lotsmall.cn/image/20190420/20190420085850itoxef.jpeg?imageMogr2/thumbnail/640x/strip/quality/50"
              alt
            />
          </li>
          <li class="active">
            <router-link tag="span" :to="{ name: 'Home'}">首页</router-link>
          </li>
          <li>
            <router-link tag="span" :to="{ name: 'Home'}">博客</router-link>
          </li>
          <li>
            <router-link tag="span" :to="{ name: 'Home'}">博客</router-link>
          </li>
        </ul>
        <div class="userInfo">
          <img
            src="https://statics.lotsmall.cn/image/20190420/20190420085850itoxef.jpeg?imageMogr2/thumbnail/640x/strip/quality/50"
            alt
          />
          <i class="iconfont iconshangjiantou"></i>
          <div class="select-box">
            <div>
               <router-link tag="span" :to="{ path: '/mdeditor'}">发起提问</router-link>
            </div>
            <div>我的提问</div>
            <div>11</div>
            <div>11</div>
          </div>
        </div>
      </div>
    </div>
    <router-view />
  </div>
</template>
<script>
export default {}
</script>
<style lang="scss">

.pc-home {
  background: #f5f6f7;
  height: 100%;
}
.pc-header {
  background: #ffffff;
  box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.05);
  .box {
    width: 1200px;
    margin: 0 auto;
    .userInfo {
      float: right;
      height: 40px;
      line-height: 38px;
      position: relative;
      .select-box {
        display: none;
        position: absolute;
        top: 33px;
        right: 0;
        z-index: 99999;
        background-color: #fff;
        border-radius: 0 0 4px 4px;
        box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.1);
        width: 124px;
        padding: 8px 0;
        box-sizing: border-box;
      }
      img {
        height: 22px;
        width: 22px;
        border-radius: 50%;
        margin-top: 9px;
        float: left;
      }
      .iconshangjiantou {
        font-size: 12px;
        float: left;
        padding: 0 5px;
        padding-left: 5px;
        cursor: pointer;
        transition: all 0.5s;
        transform-origin: 50% 50%;
        // &:hover {
        //   transform: rotate(180deg);
        //   transform-origin: 50% 50%;
        // }
      }
      &:hover {
        .select-box {
          display: block;
        }
        .iconshangjiantou {
          transform: rotate(180deg);
          transform-origin: 50% 50%;
        }
      }
    }
    ul {
      float: left;
      list-style: none;
      margin: 0;
      padding: 0;
      li {
        font-size: 14px;
        color: #3d3d3d;
        float: left;
        .logo-img {
          height: 40px;
          width: 80px;
          display: block;
          margin-right: 10px;
        }
        span {
          margin-right: 6px;
          padding: 0 3px;
          height: 40px;
          display: block;
          line-height: 38px;
        }
        &.active {
          span {
            position: relative;
            &::after {
              content: '';
              position: absolute;
              left: 0;
              bottom: 0;
              height: 2px;
              width: 100%;
              background: #ca0c16;
            }
          }
        }
        &:hover {
          color: #ca0c16;
        }
      }
    }
  }
}
</style>
