<template>
  <div class="blog-detail">
    <div class="content">
      <div class="title">
        <h3>导航组件实现方式</h3>
      </div>
      <div class="publish-info clearfix">
        <div class="fl time">
          <span class="nyr">2019年05月15日</span>
          <span class="sfm">16:36:28</span>
        </div>
        <div class="fl name">张翁哈达</div>
        <div class="reader-num fl">
          <span>阅读数</span>
          <span>85</span>
        </div>
        <div class="fr">
          <a-button class="edit" size="small" @click="go('/mdeditor')">编辑</a-button>
        </div>
      </div>
      <div class="article-content">
        <div v-html="contentStr"></div>
      </div>
      <div class="comment-box">

      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      contentStr:
        '<table> <thead> <tr> <th>column1</th> <th>column2</th> <th>column3</th> </tr> </thead> <tbody> <tr> <td>content1</td> <td>content2</td> <td>content3</td> </tr> <tr> <td>column1</td> <td>column2</td> <td>column3</td> </tr> <tr> <td>-</td> <td>-</td> <td>-</td> </tr> <tr> <td>content1</td> <td>content2</td> <td>content3</td> </tr> </tbody> </table> <p>ASDSADA</p> <table> <thead> <tr> <th>column1</th> <th>column2</th> <th>column3</th> </tr> </thead> <tbody> <tr> <td>content1</td> <td>content2</td> <td>content3</td> </tr> </tbody> </table>'
    }
  },
  methods: {
    go(path) {
      this.$router.push(path)
    }
  }
}
</script>
<style lang="scss">
.blog-detail {
  background: #f5f6f7;
  padding-top: 15px;
  .content {
    width: 1200px;
    margin: 0 auto;
    padding: 0 24px 16px;
    background: #fff;
    box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.05);
    .article-content {
      padding: 10px 0;
      table {
        border-bottom: 1px solid #e9eaec;
        border-right: 1px solid #e9eaec;
        tr {
          td,
          th {
            border-top: 1px solid #e9eaec;
            border-left: 1px solid #e9eaec;
            padding: 5px 3px;
          }
          th {
            background: #f8f8f9;
          }
        }
      }
    }
    .publish-info {
      color: #858585;
      padding-bottom: 10px;
      border-bottom: 1px solid rgb(224, 224, 224);
      .name {
        margin-right: 14px;
        color: #78a5f1;
        margin-right: 14px;
        cursor: pointer;
      }
      .time {
        margin-right: 14px;
        .nyr {
          margin-right: 4px;
        }
      }
    }
    .title {
      h3 {
        font-size: 24px;
        font-weight: 600;
        padding-top: 10px;
      }
    }
  }
}
</style>
