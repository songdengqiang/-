<template>
  <div class="home">
    <header class="headerCss">
      <h4>高速卷绕机智能运维平台</h4>
      <div class="deck">
        <div></div>
        <div></div>
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
        </div>
        <div class="decoration1">
          <div></div>
          <div></div>
          <div></div>
          <div></div>
          <div></div>
        </div>
      </div>
      <div class="topBar1">
        <div class="btns">
          <div class="caidan">实时监控</div>
          <div>
            <a href="#">监控区域1</a>
            <a href="#">监控区域2</a>
            <a href="#">监控区域3</a>
          </div>
        </div>
        <div class="btns">设备信息</div>
        <div class="btns">仓储信息</div>
      </div>
      <div class="topBar2">
        <div class="btns">故障信息</div>
        <div class="btns">维修记录</div>
        <div class="btns">系统设置</div>
      </div>
    </header>
    <main class="contentInfo">
    </main>
    <footer class="footerCss">
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
  @import url("../assets/Css/home/header.css");
  @import url("../assets/Css/home/footer.css");
  @import url("../assets/Css/home/main.css");
  @import url("../assets/Css/common/decoration.css");
  @import url("../assets/Css/common/decoration1.css");
  @import url("../assets/Css/common/btn1.css");

  *{
    padding: 0;
    margin: 0;
    box-sizing: border-box;
  }
  .home{
    position: relative;
    width: 100vw;
    height: 100vh;
    overflow: hidden;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    background: black;
  }
</style>
