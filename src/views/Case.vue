<template>
  <div class="case">
    <banner img="../assets/img/bgtop.jpg" title="婚礼提前拍系列" />
    <div class="case-section" >
      <div class="case-section-content">
        <div class="case-section-content-list" v-for="(cas,index) in caseList" :key="index">
          <img v-lazy="cas.Img" />
          <div class="content-list-abstract" :class="{'abstract-active' : index%2!=1}">
            <p class="abstract-title">{{cas.title}}</p>
            <p class="abstract-content">{{cas.content}}</p>
            <div class="more">
              <router-link
                class="text-decoration"
                :to="{ name: 'casedetails', params: { id: cas.Id }}"
              >
                <span>more</span>
                <img src="../assets/img/sanjiao.png" />
              </router-link>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import Banner from "../components/Banner";
export default {
  components: {
    Banner
  },
  data() {
    return {
      loading: true,
      caseList: [
        {
          id: 9,
          Img:'https://ss0.bdstatic.com/70cFvHSh_Q1YnxGkpoWK1HF6hhy/it/u=2962860265,1940074359&fm=26&gp=0.jpg',
          userId: 1,
          title: "佛山保利洲际| 回味婚礼电影快剪出品",
          description: "事务是应用程序中一系列严密的操作，所有操作必须成功完成，否则在每个操作中所作的所有更改都会被撤消。也就是事务具有原子性，一个事务中的一系列的操作要么全部成功，要么一个都不做。\n\n事务的结束有两种，当事务中的所以步骤全部成功执行时，事务提交。如果其中一个步骤失败，将发生回滚操作，撤消撤消之前到事务开始时的所以操作。",
          content: "一切等待都是值得的",
          created: "2021-03-06",
          status: "0"
        },
        {
          id: 7,
          userId: 1,
          Img:'https://ss0.bdstatic.com/70cFuHSh_Q1YnxGkpoWK1HF6hhy/it/u=3695025683,1043579805&fm=26&gp=0.jpg',
          title: "[我在你眼里,你在我心里] HAI & DANY| 回味婚礼电影快剪",
          description: "单例模式可能是代码最少的模式了，但是少不一定意味着简单，想要用好、用对单例模式，还真得费一番脑筋。本文对 Java 中常见的单例模式写法做了一个总结，如有错漏之处，恳请读者指正。",
          content: "一切等待都是值得的",
          created: "2021-03-06",
          status: "0"
        },
        {
          id: 3,
          Img:'https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fa0.att.hudong.com%2F22%2F76%2F01300542045786137118766392061_s.jpg&refer=http%3A%2F%2Fa0.att.hudong.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=jpeg?sec=1617613994&t=0004055ae8a9c6d77d8e6e919f2f4f4e',
          userId: 1,
          title: "[从赛道到礼堂] 兔兔&嘉乐 | 回味婚礼电影快剪",
          description: "视频中所用到的xshell和navicat直接获取哈！",
          content: "一切等待都是值得的",
          created: "2021-03-06",
          status: "0"
        },
        {
          id: 2,
          Img:'https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fpic116.nipic.com%2Ffile%2F20161201%2F22596005_115552910000_2.jpg&refer=http%3A%2F%2Fpic116.nipic.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=jpeg?sec=1617613994&t=cfc02ec3c18d53b84a4bb91fa7efdad6',
          userId: 1,
          title: "万富希尔顿| 回味婚礼电影快剪出品",
          description: "eblog是一个基于Springboot2.1.2开发的博客学习项目，为了让项目融合更多的知识点，达到学习目的，编写了详细的从0到1开发文档。主要学习包括：自定义Freemarker标签，使用shiro+redis完成了会话共享，redis的zset结构完成本周热议排行榜，t-io+websocket完成即时消息通知和群聊，rabbitmq+elasticsearch完成博客内容搜索引擎等。值得学习的地方很多！",
          content: "一切等待都是值得的",
          created: "2021-03-06",
          status: "0"
        },
        {
          id: 1,
          Img:'https://ss3.bdstatic.com/70cFv8Sh_Q1YnxGkpoWK1HF6hhy/it/u=1205618732,1920574615&fm=26&gp=0.jpg',
          userId: 1,
          title: "南沙游艇会| 回味婚礼电影快剪出品",
          description: "这里是摘要哈哈哈",
          content: "一切等待都是值得的",
          created: "2021-03-06",
          status: "0"
        }
      ],

    };
  },
  mounted() {
    // window.console.log("case");
    // this.$http
    //   .get("http:localhost:8081/blogs/?currentPage=1")
    //   .then(response => {
    //     //console.log(response);
    //     this.caseList = response.data.data.records;
    //     //window.console.log(this.caseList);
    //     this.loading = false;
    //   })
    //   .catch(function(error) {
    //     window.console.log(error);
    //   });
  }
};
</script>

 <style lang="scss" scoped>
.case {
  width: 100%;
  height: 100%;
  position: relative;
  overflow: hidden;
  background-color: #14679f;

  &-section {
    width: 100%;
    &-content {
      width: 1240px;
      min-height: 1000px;
      margin: 0 auto;
      background-color: #fff;

      &-list {
        width: 100%;
        height: 500px;
        display: flex;
        justify-content: center;
        align-items: center;
        border: 1px solid pink;

        img {
          width: 612px;
          height: 314px;
        }
        .content-list-abstract {
          width: 290px;
          height: 350px;
          padding: 0 20px;
          display: flex;
          flex-direction: column;
          justify-content: space-around;
          .abstract-title {
            line-height: 30px;
            font-size: 22px;
            color: #e13834;
          }
          .abstract-content {
            height: 150px;
            color: #484848;
            font-size: 15px;

            overflow: hidden;
            text-overflow: ellipsis;
            display: -webkit-box;
            -webkit-line-clamp: 7;
            -webkit-box-orient: vertical;
            white-space: normal !important;
            word-wrap: break-word;
            //border: 1px solid pink;
          }
          .more {
            display: flex;
            justify-content: flex-start;
            .text-decoration {
              text-decoration: none;

              span {
                color: #000;
              }
              img {
                width: 12px;
                height: 12px;
              }
            }
          }
        }
        .abstract-active {
          order: -1;
        }
      }
    }
  }
}
</style>