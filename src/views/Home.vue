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
      <div class="topBar topBar1">
        <div class="btns">
          <div class="caidan">实时监控</div>
        </div>
        <div class="btns">设备信息</div>
        <div class="btns">仓储信息</div>
      </div>
      <div class="topBar topBar2">
        <div class="btns">故障信息</div>
        <div class="btns">维修记录</div>
        <div class="btns">系统设置</div>
      </div>
    </header>
    <main class="contentInfo">
      <div class="leftBar">
        <div>
          <table>
            <tr>
              <th>基础信息</th>
            </tr>
            <tr>
              <td>纺丝产线</td>
              <td>L1</td>
            </tr>
            <tr>
              <td>纺丝位号</td>
              <td>21</td>
            </tr>
            <tr>
              <td>纺丝速度(m/min)</td>
              <td>3160</td>
            </tr>
            <tr>
              <td>剩余时间(sec)</td>
              <td>8678</td>
            </tr>
            <tr>
              <td>当前卷径(mm)</td>
              <td>319</td>
            </tr>
            <tr>
              <td>络筒时间</td>
              <td>16:02:54</td>
            </tr>
            <tr>
              <td>丝线品种</td>
              <td>经纶 0.05</td>
            </tr>
          </table>
        </div>
        <div></div>
      </div>
      <div class="centerBar">
        <div class="headerInfo">
          <div class="titleIcon">
            <img src="../assets/img/设备监控.svg" alt="图标">
            <div>设备的选择</div>
          </div>
          <div>Map OverView</div>
          <div>设备介绍</div>
        </div>
        <div class="deviceImg">
          <img src="../assets/img/device.jpg" alt="设备">
        </div>
        <div></div>
      </div>
      <div class="rightBar"></div>
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
/* 头部样式的设置 */
  @import url("../assets/Css/home/header.css");
  @import url("../assets/Css/home/footer.css");
  @import url("../assets/Css/common/decoration.css");
  @import url("../assets/Css/common/decoration1.css");
  @import url("../assets/Css/common/btn1.css");
/* 主体内容的设置 */
  @import url("../assets/Css/home/main.css");

/* 尾部样式的设置 */

/* 全局样式的设置 */
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
