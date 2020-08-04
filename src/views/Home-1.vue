<template>
  <div class="home">
    <header>
      <div class="color"></div>
      <h4>高速卷绕机智能运维平台</h4>
      <div class="decoration">
        <div></div>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
      </div>
      <div class="decoration1">
        <div></div>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
      </div>
      <div class="decoration2">
        <div></div>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
      </div>
      <div class="decoration3">
        <div></div>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
      </div>
      <!-- 选择菜单1 -->
      <div class="btn btn1">
        <div class="caidan">实时监控</div>
        <div>
          <a href="#">监控区域1</a>
          <a href="#">监控区域2</a>
          <a href="#">监控区域3</a>
        </div>
      </div>
      <!-- 选择菜单2 -->
      <div class="btn btn2">
        <div class="caidan">设备信息</div>
        <div>
          <a href="#">设备1</a>
          <a href="#">设备2</a>
          <a href="#">设备3</a>
        </div>
      </div>
      <!-- 选择菜单3 -->
      <div class="btn btn3">
        <div class="caidan">仓储信息</div>
        <div>
          <a href="#">仓储1</a>
          <a href="#">仓储2</a>
          <a href="#">仓储3</a>
        </div>
      </div>
      <!-- 选择菜单4 -->
      <div class="btn btn4">
        <div class="caidan">故障维修信息</div>
        <div>
          <a href="#">故障信息</a>
          <a href="#">维修记录</a>
        </div>
      </div>
    </header>
    <main>

    </main>
    <footer>
      <h6>系统的设置</h6>
      <h6>东华大学机械工程智能制造研究所</h6>
      <h6 >日期：{{times}}</h6>
    </footer>
  </div>
</template>

<script>
import * as d3 from 'd3'
export default {
  name: 'Home',
  components: {
  },
  data () {
    return {
      times: '',
      workShip: '车间1',
      workShipNum: 0
    }
  },
  methods: {
    // 时间的格式化
    getTime () {
      var strictIsoParse = d3.timeFormat('%m/%d/%Y-%H:%M:%S')
      this.times = strictIsoParse(new Date())
    }
    // 车间的切换
  },
  watch: {
  },
  mounted () {
    // 页面时间的定义
    setInterval(() => {
      this.getTime()
    }, 1000)
  }
}
</script>

<style scoped>
  *{
    padding: 0;
    margin: 0;
    box-sizing: border-box;
    background-color: #0a163a;
  }
  .home{
    width: 100vw;
    height: 100vh;
    overflow: hidden;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    background: rgb(82, 104, 60);
  }

  /* main{
    flex-grow: 1
  } */
  /* 头部样式的引用 */
  .color{
      width: 200vw;
      height: 1px;
      position: absolute;
      background: linear-gradient(to right,yellow,#59cdf7,rgb(40, 153, 187),green,yellow);
      z-index: 1;
      top: 3px;
      left: 100vw;
      animation: dea 4s infinite ;
  }
  @keyframes dea{
    0%{
       left: -200vw;
    };
    50%{
      left:0;
    };
    100%{
      left:200vw;
    }
  }

  @import url("../assets/Css/common/header.css");
  @import url("../assets/Css/common/decoration.css");
  @import url("../assets/Css/common/decoration1.css");
  @import url("../assets/Css/common/decoration2.css");
  @import url("../assets/Css/common/btn1.css");

  /* 中间内容的分布 */
  main{
    box-sizing: border-box;
    position: relative;
    top: 0.5vh;
    bottom: 1vh;
    width: 100vw;
    flex-grow: 1;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
  }
  .info{
    width: 100%;
    height: 25px;
    background-color: #59cdf7;
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
  }
  .content{
    width: 100%;
    /* height: 100%; */
    /* background-color: #80fed4; */
  }
  .circle{
    width: 10px;
    height: 10px;
    border-radius: 5px;
    background-color:greenyellow;
  }
  img{
    width: 100%;
    cursor: pointer
  /* margin-top: 15px */
  }

  /* main2的设置 */
  .headerInfo{
    position: relative;
    width: 100%;
    height: 4%;
    /* background-color: greenyellow; */
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
    align-items: center;
  }
  .headerInfo>div{
    position: relative;
    width: 19%;
    height: 100%;
    color: cornsilk;
    font-size: 1.05rem;
    cursor: pointer;
    background: rgb(27, 27, 27);
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
  .btn5>div{
    position: relative;
    width: 100%;
    border: none;
    color: white;
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
    align-items: center;
    z-index: 1;
}
  .btn5>div:nth-child(1){
    position: absolute;
    width: 100%;
    background:rgb(27, 27, 27) ;
    color: white;
  }
  .btn5>div:nth-child(2){
    width: 100%;
    position: absolute;
    background:rgb(27, 27, 27) ;
    top: 100%;
    opacity: 1;
    transform: scale(0);
    transition: 0.8s;
  }
  .btn5>div:nth-child(2)>a{
    margin-top: 4px;
    color: whitesmoke;
    text-decoration: none;
    border-top: #59cdf7 1px solid;
    border-bottom: #59cdf7 1px solid;
    border-left: #59cdf7 1px solid;
    border-right: #59cdf7 1px solid;
    border-radius: 4px;
    width: 100%;
  }
  .btn5>div:nth-child(2)>a:hover{
      background-color: #2a6087;
  }
  .btn5:hover :nth-child(2){
      transform: scale(1);
  }
  .contentInfo{
    position: relative;
    width: 100%;
    height: 86%;
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
    align-items: center;
    /* background-color: greenyellow; */
  }
  .contentInfo>div{
    position: relative;
    /* background: red; */
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
}
.contentInfo>div:nth-child(1){
    position: relative;
    width: 49%;
    height: 100%;
}
.contentInfo>div:nth-child(2){
    width: 49%;
    height: 100%;
    /* border: green 1px solid; */
}
.tab1{
   position: absolute;
    /* border: rosybrown 1px solid; */
    width: 100%;
    height: 98%;
    /* border-radius: 2px;
    box-shadow: gray 0 0 10px; */
}
.tab1>tr{
    position: relative;
   width: 100%;
    height: 12%;
    display: flex;
    flex-direction: row;
    color: white;
    justify-content:space-between;
    align-items: center;
    /* text-align: left;
    border-bottom: gray 1px solid; */
}
.tab1>tr>td:nth-child(1){
  width: 30%;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}
.tab1>tr>td:nth-child(2){
  width: 70%;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}
.td1{
  width: 10%;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}
.td2{
   width: 70%;
  height: 100%;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}
.td2>div{
  /* position: absolute; */
  width: 100%;
  height: 100%;
  background: rgb(69, 78, 59);
}
  .footerInfo{
    position: relative;
    width: 100%;
    height: 8%;
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
      /* background-color: greenyellow; */
  }
  .footerInfo>div{
    width: 50%;
    height: 100%;
    color: aliceblue;
  }

  @import url("../assets/Css/common/main.css");
  /* 尾部样式的引用 */
  footer{
    box-sizing: border-box;
    height: 3vh;
    width: 100vw;
    border-top: #59cdf7 2px solid;
    position: relative;
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
    align-items: center;
    color: white;
    /* padding: 15px */
    box-shadow: aquamarine 0 0 5px;
    padding-right: 15px;
    padding-left: 15px
  }
  @import url("../assets/Css/common/footer.css");
</style>
