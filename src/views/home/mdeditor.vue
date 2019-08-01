<template>
  <div class="mdeditor-page">
    <div class="txt-bar clearfix">
      <div class="bar fl">
        <input type="text" placeholder="请输入文章标题" />
      </div>
      <div class="submit-bar fr clearfix">
        <img
          class="fr"
          src="https://statics.lotsmall.cn/image/20190420/20190420085850itoxef.jpeg?imageMogr2/thumbnail/640x/strip/quality/50"
          alt
        />
        <a-button class="submit-btn fr" type="primary">提交问题</a-button>
      </div>
    </div>
    <mavon-editor :ishljs="true"></mavon-editor>
  </div>
</template>
<style lang='scss'>
.mdeditor-page {
  .txt-bar {
    .submit-bar {
      padding-right: 20px;
      margin-top: 13.5px;
      .submit-btn {
        margin-right: 10px;
      }
      img {
        height: 32px;
        width: 32px;
        border-radius: 50%;
        display: block;
      }
    }
    .bar {
      padding: 10px 20px;
      width: calc(100% - 200px);
      input {
        width: 100%;
        outline: none;
        border: 1px solid #ccc;
        font-size: 18px;
        padding: 5px 20px;
        border-radius: 4px;
      }
    }
  }
}
</style>
