<template>
  <div>
    <!-- 顶部区域 -->
    <header class="header">
      <div class="header-top">
        <!-- logo区域 -->
        <div class="logo-w">
          <a class="logo" href="https://www.jiakaobaodian.com/"></a>
        </div>
        <!-- 搜索框 -->
        <div class="search-w">
          <form action="https://www.so.com/s" target="_blank" id="so360form">
            <input
              type="text"
              placeholder="请输入关键字"
              autocomplete="off"
              name="q"
              id="so360_keyword"
              class="search-input"
            />
            <input
              type="submit"
              class="button"
              ref="soSubmit"
              id="so360_submit"
              value="搜 索"
            />
            <input type="hidden" name="ie" value="utf8" /><input
              type="hidden"
              name="src"
              value="zz_jiakaobaodian.com"
            /><input type="hidden" name="site" value="jiakaobaodian.com" />
            <input type="hidden" name="rg" value="1" />
          </form>
        </div>
      </div>
      <!-- 导航栏 -->
      <nav class="horizontal-nav">
        <ul class="nav-w">
          <li>
            <a
              @click="selectNavItem('home')"
              :class="{ active: selectedNavItem === 'home' }"
              href="https://www.jiakaobaodian.com/"
              >首页</a
            >
          </li>
          <li class="menu-jx" @click="selectNavItem('mnks')">
            <a
              class=""
              href="https://www.jiakaobaodian.com/mnks/"
              :class="{ active: selectedNavItem === 'mnks' }"
              >模拟考试</a
            >
            <div class="drop-w">
              <a href="https://www.jiakaobaodian.com/mnks/kemu1/car.html"
                >科目一</a
              >
              <a href="https://www.jiakaobaodian.com/mnks/kemu2/car.html"
                >科目二</a
              >
              <a href="https://www.jiakaobaodian.com/mnks/kemu3/car.html"
                >科目三</a
              >
              <a href="https://www.jiakaobaodian.com/mnks/kemu4/car.html"
                >科目四</a
              >
            </div>
          </li>
          <li class="menu-jx" @click="selectNavItem('school')">
            <a
              href="https://www.jiakaobaodian.com/school/"
              :class="{ active: selectedNavItem === 'school' }"
              >找驾校</a
            >
            <div class="drop-w">
              <a href="https://www.jiakaobaodian.com/school/">找驾校</a>
              <a href="https://www.jiakaobaodian.com/coach/">找教练</a>
              <a href="https://www.jiakaobaodian.com/peilian/">找陪练</a>
            </div>
          </li>
          <li>
            <a
              class=""
              href="https://www.jiakaobaodian.com/bbs/"
              @click="selectNavItem('bbs')"
              :class="{ active: selectedNavItem === 'bbs' }"
              >驾考圈</a
            >
          </li>
          <li>
            <a
              class=""
              href="https://www.jiakaobaodian.com/sign/"
              @click="selectNavItem('sign')"
              :class="{ active: selectedNavItem === 'sign' }"
              >交通标志</a
            >
          </li>
          <li>
            <a
              class=""
              href="https://www.jiakaobaodian.com/download/"
              @click="selectNavItem('download')"
              :class="{ active: selectedNavItem === 'download' }"
              >软件下载</a
            >
          </li>
          <li class="qiye">
            <a
              href="https://qiye.jiakaobaodian.com"
              target="_blank"
              rel="nofollow"
              >驾考宝典企业版</a
            >
          </li>
          <li>
            <a
              href="https://www.futurephantom.cn/"
              target="_blank"
              rel="nofollow"
              >智慧驾校</a
            >
          </li>
          <li class="menu-jx">
            <a href="https://www.maiche.com/rank/?from=jiakao_web">买新车</a>
            <div class="drop-w">
              <a
                href="https://www.maiche.com/rank/?from=jiakao_web"
                target="_blank"
                rel="nofollow"
                >买车网</a
              ><a href="http://www.pingxing.cn" target="_blank" rel="nofollow"
                >平行之家</a
              >
            </div>
          </li>
          <li>
            <a
              href="http://www.xiaozhu2.com/?from=jiakao_web"
              target="_blank"
              rel="nofollow"
              >二手车</a
            >
          </li>
        </ul>
      </nav>
    </header>

    <!-- 轮播图 -->
    <div class="carousel">
      <Carousel />
    </div>

    <!-- 内容区域 -->
    <div class="container">
      <div class="container-title">
        <hr class="hr" />
        <div class="title-text">2024小车理论考试</div>
      </div>
      <div class="container-content">
        <ul class="item km left">
          <li class="item-right">
            <a
              class="link"
              target="_blank"
              href="https://www.jiakaobaodian.com/mnks/kemu1/car.html"
              >科目一交规<span class="small"></span>
            </a>
          </li>
          <li class="item-left icon1">
            <a
              target="_blank"
              href="https://www.jiakaobaodian.com/mnks/exercise/0-car-kemu1.html"
              >顺序练习</a
            >
            <p>按照顺序练习做题</p>
          </li>
          <li class="item-left icon2">
            <a
              target="_blank"
              href="https://www.jiakaobaodian.com/mnks/exercise/3-car-kemu1.html"
              >随机练习</a
            >
            <p>按随机顺序做题</p>
          </li>
          <li class="item-left icon3">
            <a
              target="_blank"
              href="https://www.jiakaobaodian.com/mnks/strengthen/car-kemu1.html"
              >专项练习</a
            >
            <p>分门别类重点突破</p>
          </li>
          <li class="item-left icon4">
            <a
              target="_blank"
              href="https://www.jiakaobaodian.com/mnks/exercise/8-car-kemu1.html"
              >难题攻克</a
            >
            <p>准确把握考试难点</p>
          </li>
          <li class="item-right btn-bar">
            <a
              class="btn-link"
              target="_blank"
              href="https://www.jiakaobaodian.com/mnks/exam/car-kemu1.html"
              >模拟考试</a
            >
          </li>
        </ul>
        <ul class="item km right">
          <li class="item-right">
            <a
              class="link"
              target="_blank"
              href="https://www.jiakaobaodian.com/mnks/kemu4/car.html"
              >科目四安全文明驾驶<span class="small"></span
            ></a>
          </li>
          <li class="item-left icon1">
            <a
              target="_blank"
              href="https://www.jiakaobaodian.com/mnks/exercise/0-car-kemu3.html"
              >顺序练习</a
            >
            <p>按照顺序练习做题</p>
          </li>
          <li class="item-left icon2">
            <a
              target="_blank"
              href="https://www.jiakaobaodian.com/mnks/exercise/3-car-kemu3.html"
              >随机练习</a
            >
            <p>按随机顺序做题</p>
          </li>
          <li class="item-left icon3">
            <a
              target="_blank"
              href="https://www.jiakaobaodian.com/mnks/strengthen/car-kemu3.html"
              >专项练习</a
            >
            <p>分门别类重点突破</p>
          </li>
          <li class="item-left icon4">
            <a
              target="_blank"
              href="https://www.jiakaobaodian.com/mnks/exercise/8-car-kemu3.html"
              >难题攻克</a
            >
            <p>准确把握考试难点</p>
          </li>
          <li class="item-right btn-bar">
            <a
              class="btn-link"
              target="_blank"
              href="https://www.jiakaobaodian.com/mnks/exam/car-kemu3.html"
              >模拟考试</a
            >
          </li>
        </ul>
      </div>
    </div>

    <div class="footer">
      <!-- 入驻 -->
      <div class="banner-mid-ad com-part-home">
        <a
          target="_blank"
          href="https://saas-shop.jiakaobaodian.com/runtu/cooperate.html"
        >
          <img src="../images/banner-jxb.png" />
        </a>
      </div>
    </div>

    <!-- 驾校推荐 -->
    <div class="part-home">
      <div class="part-home-title">
        <hr class="hr" />
        <div class="title-text">驾校推荐</div>
        <div class="title-text2"></div>
      </div>
      <div class="jiaoxiao-tuijian-container">
        <ul class="school-list clearfix">
          <li>
            <div class="item-top clearfix">
              <div class="col1 left">
                <div class="div1">
                  <span class="name">龙泉驾校</span>
                  <div class="star-w-s">
                    <div class="bfb" style="width: 84%"></div>
                  </div>
                </div>
                <div class="div2">
                  <span>口碑好</span><span>规模大</span><span>拿本快</span
                  ><span>包接送</span>
                </div>
              </div>
              <div class="col2 left">
                <p class="price red">￥3480</p>
              </div>
              <div class="col3 right">
                <button class="btn-baoming" ref="baoming" data-id="8567">
                  学车报名
                </button>
              </div>
            </div>
            <div class="item-content">
              <div class="img-w">
                <img
                  src="https://avatar-user.mucang.cn/user-avatar/default/fxOE7y8HmQ8.jpg!100x100"
                />
              </div>
              <p class="content">
                新手听教练的就完事了，我自己出现的问题是一档起步和加挡给油有问题，索性最后搞定了，希望帮到大家
              </p>
            </div>
            <div class="tip"></div>
          </li>
          <li>
            <div class="item-top clearfix">
              <div class="col1 left">
                <div class="div1">
                  <span class="name">公交驾校</span>
                  <div class="star-w-s">
                    <div class="bfb" style="width: 88.00000000000001%"></div>
                  </div>
                </div>
                <div class="div2">
                  <span>口碑好</span><span>规模大</span><span>拿本快</span
                  ><span>包接送</span>
                </div>
              </div>
              <div class="col2 left">
                <p class="price red">￥4900</p>
              </div>
              <div class="col3 right">
                <button class="btn-baoming" ref="baoming" data-id="15288">
                  学车报名
                </button>
              </div>
            </div>
            <div class="item-content">
              <div class="img-w">
                <img
                  src="https://avatar-user.mc-cdn.cn/user-avatar/2024/03/16/19/ac92fae755794ff6a6f5fff0b9343f71.jpg!100x100"
                />
              </div>
              <p class="content">不错啊还行不错好</p>
            </div>
            <div class="tip"></div>
          </li>
          <li>
            <div class="item-top clearfix">
              <div class="col1 left">
                <div class="div1">
                  <span class="name">嘉安驾校</span>
                  <div class="star-w-s">
                    <div class="bfb" style="width: 91.99999999999999%"></div>
                  </div>
                </div>
                <div class="div2">
                  <span>口碑好</span><span>规模大</span><span>拿本快</span
                  ><span>包接送</span>
                </div>
              </div>
              <div class="col2 left">
                <p class="price red">￥4000</p>
              </div>
              <div class="col3 right">
                <button class="btn-baoming" ref="baoming" data-id="47127">
                  学车报名
                </button>
              </div>
            </div>
            <div class="item-content">
              <div class="img-w">
                <img
                  src="https://avatar-user.mucang.cn/user-avatar/default/adK3Vu70DEQ.jpg!100x100"
                />
              </div>
              <p class="content">。。。。。。。。</p>
            </div>
            <div class="tip"></div>
          </li>
          <li>
            <div class="item-top clearfix">
              <div class="col1 left">
                <div class="div1">
                  <span class="name">远大驾校</span>
                  <div class="star-w-s">
                    <div class="bfb" style="width: 86%"></div>
                  </div>
                </div>
                <div class="div2">
                  <span>口碑好</span><span>规模大</span><span>拿本快</span
                  ><span>包接送</span>
                </div>
              </div>
              <div class="col2 left">
                <p class="price red">￥3480</p>
              </div>
              <div class="col3 right">
                <button class="btn-baoming" ref="baoming" data-id="8577">
                  学车报名
                </button>
              </div>
            </div>
            <div class="item-content">
              <div class="img-w">
                <img
                  src="https://avatar-user.mucang.cn/user-avatar/default/jgYPG6pZzPc.jpg!100x100"
                />
              </div>
              <p class="content">
                科二体验相当不错，前四天是模拟器VR练车，有充足的时间熟悉操作，后三天是实车，但也是有ai在旁边指导纠错。考前有考场模拟，从练车到考试车里只有自己，我自己反正觉得这样很好，考试时候不会紧张。
              </p>
            </div>
            <div class="tip"></div>
          </li>
        </ul>
        <div class="btn-bar">
          <a target="_blank" href="https://www.jiakaobaodian.com/school/"
            >查看更多</a
          >
        </div>
      </div>
    </div>
    <!-- 学车流程 -->
    <div class="com-home-study-step part-home">
      <div class="part-home-title">
        <hr class="hr" />
        <div class="title-text">学车流程</div>
        <div class="title-text2">
          驾考宝典整合学车全流程，驾考宝典为用户提供全方位学车服务
        </div>
      </div>
      <div class="content">
        <ul class="item clearfix">
          <li class="item-left icon1">
            <a target="_blank" href="https://www.jiakaobaodian.com/school/"
              ><span class="title">找驾校</span>
              <p>口碑好的驾校</p>
            </a>
          </li>
          <li class="item-left icon2">
            <a
              target="_blank"
              href="https://www.jiakaobaodian.com/mnks/kemu1/car.html"
              ><span class="title">科目一</span>
              <p>驾驶员理论考试</p>
            </a>
          </li>
          <li class="item-left icon3">
            <a
              target="_blank"
              href="https://www.jiakaobaodian.com/mnks/kemu2/car.html"
              ><span class="title">科目二</span>
              <p>场地驾驶技能考试科目</p>
            </a>
          </li>
          <li class="item-left icon4">
            <a
              target="_blank"
              href="https://www.jiakaobaodian.com/mnks/kemu3/car.html"
              ><span class="title">科目三</span>
              <p>机动车驾驶人道路考试</p>
            </a>
          </li>
          <li class="item-left icon5">
            <a
              target="_blank"
              href="https://www.jiakaobaodian.com/mnks/kemu4/car.html"
              ><span class="title">科目四</span>
              <p>安全文明驾驶常识考试</p>
            </a>
          </li>
          <li class="item-left icon6">
            <a href="javascript:;"
              ><span class="title">拿本</span>
              <p>开心拿本，安全驾驶</p>
            </a>
          </li>
        </ul>
      </div>
    </div>
    <!-- 宝典荣誉 -->
    <div class="part-home">
      <div class="part-home-title">
        <hr class="hr" />
        <div class="title-text">宝典荣誉</div>
        <div class="title-text2">
          强大的驾考功能，优秀的用户体验，我们的愿景是学车无忧，轻松拿本
        </div>
      </div>
      <div class="content"><img src="../images/home-dynamic.png" /></div>
    </div>

    <!-- 驾考宝典app -->
    <div class="com-home-app-ad">
      <div class="content">
        <div class="ad1">
          <span>教练宝典APP</span>
          <div></div>
        </div>
        <div class="ad2">
          <span>驾考宝典APP</span>
          <div></div>
        </div>
        <div class="ad3">
          <span>买车宝典APP</span>
          <div></div>
        </div>
      </div>
    </div>

    <!-- 下载 -->
    <div class="com-home-app-down part-home">
      <div class="content">
        <ul class="item clearfix">
          <li class="item-left">
            <span>驾考宝典APP下载</span>
            <p>考驾照 用宝典</p>
          </li>
          <li class="item-left right">
            <span>驾考宝典微信小程序</span>
            <p>无需下载，驾考做题更方便！</p>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
// 导入轮播图组件
import Carousel from "./Carousel.vue";
export default {
  components: {
    Carousel,
  },
  name: "HelloWorld",
  data() {
    return {
      selectedNavItem: "",
    };
  },
  methods: {
    selectNavItem(item) {
      this.selectedNavItem = item;
    },
  },
};
</script>

<style scoped lang="less">
header {
  height: 148px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-between;
}

header .header-top {
  width: 1200px;
  height: 42px;
  margin: 28px auto;
  display: flex;
  justify-content: space-between;
  align-items: center;

  .logo-w {
    width: 207px;
    height: 100%;
    overflow: hidden;
    font-size: 36px;

    .logo {
      display: block;
      width: 207px;
      height: 100%;
      background: url(../images/logo.png) left center no-repeat;
    }
  }

  .search-w {
    position: relative;
    width: 300px;

    input {
      float: left;
      height: 42px;
      width: 100%;
      line-height: 40px;
      border: 1px solid #e9e9e9;
      font-size: 14px;
      padding: 0 40px 0 10px;
    }

    .button {
      position: absolute !important;
      top: 0 !important;
      right: 0 !important;
      width: 14% !important;
    }
  }

  input:focus {
    outline: none;
    border: 1px solid #007aff;
    /* 输入框获得焦点时的边框颜色 */
  }
}

.horizontal-nav {
  width: 100%;
  height: 50px;
  background-color: #37b5f8;
  color: #fff;

  .nav-w {
    width: 1200px;
    margin: auto;
    height: 50px;
    line-height: 50px;
    font-size: 16px;
    text-align: left;

    .qiye {
      width: 148px;
    }

    .menu-jx {
      position: relative;
      overflow: visible;

      > a:after {
        display: inline-block;
        vertical-align: middle;
        width: 10px;
        height: 10px;
        margin-left: 6px;
        margin-top: 5px;
        border: 5px solid transparent;
        border-top: 5px solid #fff;
        content: " ";
      }

      .drop-w {
        font-size: 14px;
        display: none;
        position: absolute;
        top: 50px;
        width: 100%;
        background-color: #fff;
        z-index: 2;
        line-height: 40px;
        padding: 0 8px;
        color: #666;
        box-shadow: 0 0 20px rgba(0, 0, 0, 0.1);

        > a:hover {
          color: #37b5f9;
        }
      }
    }

    .menu-jx:hover .drop-w {
      display: block;
    }

    > li:hover {
      background-color: #54c0f9;
    }

    > li {
      display: inline-block;
      padding: 0;
      vertical-align: top;
      width: 108px;
      text-align: center;

      a {
        display: block;
        height: 100%;
        width: 100%;
      }

      .active {
        background-color: #258fc7;
      }
    }
  }
}

.container {
  width: 1200px;
  margin: 60px auto;

  //鼠标悬停
  a:hover {
    color: #37b5f8;
  }

  //清除浮动
  > .container-content::after {
    clear: both;
    display: table;
    content: " ";
  }

  > .container-content ul.item.km {
    border: 1px solid #e9e9e9;
    width: 580px;

    > li.item-right {
      width: 100%;
      height: 110px;
      line-height: 110px;
      padding-top: 0;
      border: none;
      margin: 0;
      text-align: center;

      > a.link {
        padding: 0 0 0 38px;
        display: inline-block;
        background: url(../images/content1.png) left center no-repeat;
        font-size: 20px;
        font-family: "Microsoft YaHei", "Hiragino Sans GB",
          "Hiragino Sans GB W3", "Helvetica Neue", Helvetica, Arial, sans-serif;
      }

      > .btn-link {
        width: 300px;
        margin: 15px auto 30px;
        border: none;
        display: block;
        height: 46px;
        line-height: 44px;
        background: #37b5f8;
        color: #fff;
        border-radius: 4px;
      }
    }

    > li.item-right.btn-bar {
      height: auto;
      line-height: 70px;
      float: left;
    }

    > li.item-left {
      float: left;
      width: 250px;
      height: 70px;
      line-height: 20px;
      margin: 0 0 15px 25px;
      padding: 15px 0 15px 85px;
      background-color: #fafafa;

      > a {
        font-size: 16px;

        font-family: "Microsoft YaHei", "Hiragino Sans GB",
          "Hiragino Sans GB W3", "Helvetica Neue", Helvetica, Arial, sans-serif;
      }

      > p {
        color: #999;
      }
    }

    //less插值
    .generate-icons(@n, @total) when (@n =< @total) {
      .icon@{n} {
        background: ~"url(../images/icon@{n}.png) left 50px center no-repeat";
      }

      .generate-icons(@n + 1, @total);
    }

    .generate-icons(1, 4); // 调用 mixin 生成四个图标样式
  }

  > .container-title {
    margin-bottom: 40px;
    text-align: center;
    padding-top: 20px;

    > .hr {
      height: 1px;
      border: none;
      border-top: 1px dotted #e9e9e9;
    }

    > .title-text {
      display: inline-block;
      margin-top: -20px;
      line-height: 41px;
      padding: 0 45px;
      background-color: #fff;
      font-size: 30px;
    }
  }
}

.footer .banner-mid-ad.com-part-home {
  margin-top: -30px;
  width: 1200px;
  margin: 60px auto;
}

.part-home {
  width: 1200px;
  margin: 60px auto;

  > .part-home-title {
    margin-bottom: 40px;
    text-align: center;
    padding-top: 20px;

    > .hr {
      height: 1px;
      border: none;
      border-top: 2px dotted red;
    }

    > .title-text {
      display: block;
      margin-top: -16px;
      line-height: 41px;
      padding: 0 45px;
      background-color: #fff;
      font-size: 30px;
    }

    > .title-text2 {
      font-size: 16px;
      margin: 30px 0;
      color: #666;
    }
  }

  > .jiaoxiao-tuijian-container {
    margin: 0 auto;

    > .school-list {
      margin: -30px 0 0 -30px;
      color: #666;
      font-size: 14px;
      font-family: "Microsoft YaHei", "Hiragino Sans GB", "Hiragino Sans GB W3",
        "Helvetica Neue", Helvetica, Arial, sans-serif;

      > li {
        float: left;
        position: relative;
        width: 585px;
        margin: 30px 0 0 30px;
        padding: 40px 30px;
        border: 1px solid #e9e9e9;

        > .item-content {
          height: 80px;
          margin-top: 30px;
          padding: 20px;
          background: #fafafa;
          color: #999;

          > .img-w {
            float: left;
            width: 40px;
            height: 40px;
            border-radius: 50%;

            img {
              background: 0 0;
              border: 0;
              max-width: 100%;
            }
          }

          > .content {
            height: 40px;
            line-height: 20px;
            margin-left: 60px;
            display: -webkit-box;
            overflow: hidden;
            text-overflow: ellipsis;
            -webkit-line-clamp: 2;
            line-clamp: 2;
          }
        }

        > .item-top {
          > .col1 {
            width: 305px;
            line-height: 30px;

            > .div1 {
              .name {
                max-width: 180px;
                display: inline-block;
                vertical-align: middle;
                font-size: 22px;
                overflow: hidden;
                white-space: nowrap;
                text-overflow: ellipsis;
              }

              .star-w-s {
                display: inline-block;
                vertical-align: middle;
                margin: -3px 0 0 10px;
                width: 90px;
                height: 20px;
                background: url(../files/109f416….png) left center no-repeat;

                .bfb {
                  height: 100%;
                  background: url(../images/star.png) left center no-repeat;
                }
              }
            }

            > .div2 {
              margin-top: 10px;
              line-height: 20px;

              > span {
                display: inline-block;
                background: url(../images/good.png) left center no-repeat;
                padding-left: 20px;
              }

              //第二个span开始
              > span:nth-child(n + 2) {
                margin-left: 10px;
              }
            }
          }

          > .col2 {
            width: 130px;
            line-height: 63px;
            border-left: 1px solid #e9e9e9;
            font-size: 30px;
            text-align: center;
          }

          > .col3 button {
            width: 80px;
            line-height: 28px;
            margin-top: 17px;
            text-align: center;
            font-size: 14px;
            border-radius: 4px;
          }
        }

        > .item-top::after {
          clear: both;
          display: block;
          content: "";
        }

        > .tip {
          position: absolute;
          top: 5px;
          right: 10px;
        }
      }
    }

    > .btn-bar {
      margin-top: 40px;

      a {
        display: block;
        width: 280px;
        margin: 20px auto 0;
        line-height: 48px;
        border: 1px solid #e9e9e9;
        border-radius: 4px;
        color: #999;
        text-align: center;
        font-size: 16px;
      }

      a:hover {
        color: #37b5f8;
        border: 1px solid #37b5f8;
      }
    }
  }
}

.com-home-study-step > .content {
  text-align: center;

  ul.item {
    margin: 0 -40px;

    > li.item-left {
      float: left;
      width: 16.6%;
      line-height: 1.4;

      > a {
        display: block;
        padding: 150px 40px 0;

        > .title {
          display: block;
          font-size: 24px;
          font-family: "Microsoft YaHei", "Hiragino Sans GB",
            "Hiragino Sans GB W3", "Helvetica Neue", Helvetica, Arial,
            sans-serif;
        }

        > p {
          color: #999;
          margin: 10px -20px;
        }
      }

      > a:hover {
        color: #37b5f8;
      }
    }

    //less插值
    .generate-icons(@n, @total) when (@n =< @total) {
      .icon@{n} {
        background: ~"url(../images/x-icon@{n}.png) center top  no-repeat";
      }

      .generate-icons(@n + 1, @total);
    }

    .generate-icons(1, 6); // 调用 mixin 生成四个图标样式
  }
}

.com-home-app-ad {
  background-color: #f5f5f5;

  > .content {
    position: relative;
    width: 1200px;
    height: 560px;
    margin: 70px auto 0;
    overflow: hidden;

    div span {
      font-size: 20px;
    }

    > div {
      position: absolute;
      bottom: -40px;
      text-align: center;
      transition: transform 0.5s;
      /* 添加过渡效果，让移动更平滑 */
    }

    > div:hover {
      transform: translateY(-30px);
      /* 当鼠标悬停时，向上移动 30px */
    }

    > div:hover > div {
      display: block;
    }

    .ad1 {
      left: 30px;
      width: 300px;
      height: 500px;
      background: url(../images/app1.png) center bottom no-repeat;

      > div {
        display: none;
        width: 100%;
        height: 100%;
        margin-top: 37px;
        background: url(../images/ewm.png) center no-repeat;
      }
    }

    .ad2 {
      left: 400px;
      width: 430px;
      height: 540px;
      background: url(../images/app2.png) center bottom no-repeat;

      > div {
        display: none;
        width: 100%;
        height: 100%;
        margin-top: 52px;
        background: url(../images/ewm-plus.png) center no-repeat;
        background-color: rgba(255, 255, 255, 0.5);
        background-size: 150px 150px;
      }
    }

    .ad3 {
      left: 905px;
      width: 265px;
      height: 428px;
      background: url(../images/app3.png) center bottom no-repeat;

      > div {
        display: none;
        width: 100%;
        height: 100%;
        margin-top: 37px;
        background: url(../images/mc-ewm.png) center no-repeat;
      }
    }
  }
}

.com-home-app-down > .content ul.item > li.item-left {
  float: left;
  width: 600px;
  line-height: 1.7;
  margin: 20px 0;
  padding: 40px 80px;
  background: url(../images/ewm-plus.png) right 80px center no-repeat;
  background-size: 140px;
  border-right: 1px solid #e9e9e9;
  > span {
    font-size: 20px;
    font-family: "Microsoft YaHei", "Hiragino Sans GB", "Hiragino Sans GB W3",
      "Helvetica Neue", Helvetica, Arial, sans-serif;
  }
  > p {
    color: #999;
  }
}
.com-home-app-down > .content ul.item > li.item-left.right {
  float: right;
  background: url(../images/xcx.jpg) right 80px center no-repeat;
  background-size: 130px;
  border: none;
}
</style>
