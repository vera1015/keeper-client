<template>
  <div class="mdl-grid content">
    <!-- side panel -->
    <div class="cards mdl-cell mdl-cell--3-col mdl-cell--8-col-tablet mdl-grid">
      <my-card class="mdl-card horizon-center">
        <div slot="title" class="mdl-card__title patient-banner">
          <h2 class="mdl-card__title-text keeper-title mdl-color-text--white">病人资料</h2>
        </div>
        <div slot="media">
        </div>
        <div slot="supporting-text">
        </div>
        <div slot="actions" class="mdl-card__actions mdl-card--border mdl-color-text--grey-600">
          <img v-bind:src="headUrl" class="aid-avatar">
          <p class="patient-name secondary-text">{{ patientUsername }}</p>
          <ul class="mdl-list">
            <li class="mdl-list__item">
              <span class="mdl-list__item-primary-content">
                年龄：{{ age }}
              </span>
            </li>
            <li class="mdl-list__item">
              <span class="mdl-list__item-primary-content">
                性别：{{ sex }}
              </span>
            </li>
            <li class="mdl-list__item">
              <span class="mdl-list__item-primary-content">
                手机：{{ mobilePhoneNumber }}
              </span>
            </li>
          </ul>
        </div>
      </my-card>
      <div class="separator mdl-cell--1-col"></div>
      <my-card class="options mdl-card mdl-color--teal-600">
        <div slot="title">
        </div>
        <div slot="media">
        </div>
        <div slot="supporting-text" class="mdl-card__supporting-text mdl-color-text--blue-grey-50">
          <h3>历史记录</h3>
          <ul>
            <li>
              <label for="chkbox1" class="mdl-checkbox mdl-js-checkbox mdl-js-ripple-effect">
                <input type="checkbox" id="chkbox1" checked="true" class="mdl-checkbox__input">
                <span class="mdl-checkbox__label">2015年8月15日</span>
              </label>
            </li>
            <li>
              <label for="chkbox2" class="mdl-checkbox mdl-js-checkbox mdl-js-ripple-effect">
                <input type="checkbox" id="chkbox2" class="mdl-checkbox__input">
                <span class="mdl-checkbox__label">2015年8月15日</span>
              </label>
            </li>
            <li>
              <label for="chkbox3" class="mdl-checkbox mdl-js-checkbox mdl-js-ripple-effect">
                <input type="checkbox" id="chkbox3" class="mdl-checkbox__input">
                <span class="mdl-checkbox__label">2015年8月15日</span>
              </label>
            </li>
            <li>
              <label for="chkbox4" class="mdl-checkbox mdl-js-checkbox mdl-js-ripple-effect">
                <input type="checkbox" id="chkbox4" class="mdl-checkbox__input">
                <span class="mdl-checkbox__label">2015年8月15日</span>
              </label>
            </li>
          </ul>
        </div>
        <div slot="actions" class="mdl-card__actions mdl-card--border">
          <a href="#" class="mdl-button mdl-js-button mdl-js-ripple-effect mdl-color-text--blue-grey-50">位置信息</a>
          <div class="mdl-layout-spacer"></div>
          <i class="material-icons">location_on</i>
        </div>
      </my-card>
    </div>

    <!-- main panel -->
    <div class="cards mdl-cell mdl-cell--9-col mdl-grid">
      <my-card class='mdl-card mdl-cell--12-col'>
        <div slot="title" class="mdl-card__title mdl-color--teal-600">
          <h2 class="mdl-card__title-text keeper-title mdl-color-text--white">地图显示</h2>
        </div>
        <div slot="media">
        </div>
        <div slot="supporting-text">
        </div>
        <div slot="actions" class="mdl-card__actions mdl-card--border">
          <div id="map" class="show-chart"></div>
        </div>
      </my-card>
      <!-- <div class="separator mdl-cell--1-col"></div> -->
      <my-card class='mdl-card mdl-cell--12-col'>
        <div slot="title" class="mdl-card__title">
          <h2 class="mdl-card__title-text keeper-title">详细信息</h2>
        </div>
        <div slot="media">
        </div>
        <div slot="supporting-text">
        </div>
        <div slot="actions" class="mdl-card__actions mdl-card--border">
          <div class="mdl-grid bottom-border">
            <div class="mdl-cell mdl-cell--6-col text-center">
              <h5>急救地点</h5>
              <span class="text-muted secondary-text">四川省成都市双流县航空港长城路一段185号-好安逸大酒店</span>
            </div>
            <div class="mdl-cell mdl-cell--6-col text-center">
              <h5>病情诊断</h5>
              <span class="text-muted secondary-text">心肌梗死，并发性心律失常、休克或心力衰竭，体征</span>
            </div>
          </div>
          <div class="mdl-grid">
            <div class="mdl-cell mdl-cell--8-col">
              <h5>病人最后一次自我描述</h5>
              <span class="text-muted secondary-text">最近半个月经常。。。心律失常的生活调理方法可以根据心律失常的诱因制定。心律失常的常见诱因有：吸烟、酗酒、过劳、紧张、激动、暴饮暴食，消化不良，感冒发烧，摄入盐过多，血钾、血镁低等。这样可以做到从本质出发，从根本上对心律失常引起的病症起到控制的作用。首先，在饮食的方面：应该细嚼慢咽，这样也有助于消化吸收，对健康有益，忌狼吞虎咽。应该少饮酒，这样不会加重心脏负担，也不会增加心肌耗氧量，喝咖啡也忌大量。其次，在运动方面：运动要适量，切不可挑战极限，多做适合自己的运动，轻松舒缓的运动，少做剧烈运动。再次，在情绪方面：要学会控制自己的情绪，尽量保持平和稳定的心态，不焦不躁，遇事懂得宽慰自己，不看过激的比赛等。 因此，为了减少或避免心律失常的发生，应当注意加强生活中饮食、运动、情绪等方面的调节与护理。更多关于诱发心律失常的生活细节请咨询我们的在线专家。</span>
            </div>
            <div class="mdl-cell mdl-cell--4-col">
              <div class="bottom-border">
                <h5>心律</h5>
                <span class="text-muted secondary-text">55次/分钟</span>
              </div>
              <div>
                <h5>最近一次心电图</h5>
                <a href="">201508261213.png</a>
              </div>
            </div>
          </div>
        </div>
      </my-card>
    </div>
  </div>
</template>

<script>
  function initialize () {
    var map = new BMap.Map('map')
    var point = new BMap.Point(103.593302, 30.332618)
    var marker = new BMap.Marker(point) // 创建点

    // 百度地图API功能
    var p1 = new BMap.Point(104.0704200000, 30.6473800000)
    var p2 = new BMap.Point(103.593302, 30.332618)

    var driving = new BMap.DrivingRoute(map, {
      renderOptions: {
        map: map,
        autoViewport: true
      }
    })
    driving.search(p1, p2)

    // 坐标参数
    map.centerAndZoom(point, 15)

    map.addOverlay(marker)
    map.addControl(new BMap.NavigationControl())
    map.addControl(new BMap.ScaleControl())
    map.addControl(new BMap.OverviewMapControl())
    map.addControl(new BMap.MapTypeControl())

    var label = new BMap.Label('病人位置', {
      offset: new BMap.Size(-15, 25)
    })
    marker.setLabel(label)
  }

  function loadScript () {
    let script = document.createElement('script')

    script.src = 'http://api.map.baidu.com/api?v=2.0&ak=jD80NNGOkZPEmG5Fugcaiyoa&callback=initialize'
    document.body.appendChild(script)
  }

  import Card from '../utils/Card'

  export default {
    components: {
      'my-card': Card
    },
    data () {
      return {
        headUrl: this.$store.state.patient.currentPatient ? this.$store.state.patient.currentPatient.get('headUrl') : '/static/images/user.jpg',
        patientUsername: this.$store.state.patient.currentPatient ? this.$store.state.patient.currentPatient.get('username') : '请先登录',
        age: this.$store.state.patient.currentPatient ? this.$store.state.patient.currentPatient.get('age') : '',
        sex: this.$store.state.patient.currentPatient ? (this.$store.state.patient.currentPatient.get('sex') === 0 ? '男' : '女') : '',
        mobilePhoneNumber: this.$store.state.patient.currentPatient ? this.$store.state.patient.currentPatient.get('mobilePhoneNumber') : ''
      }
    },
    beforeRouteEnter (to, from, next) {
      // 在渲染该组件的对应路由被 confirm 前调用
      // 不！能！获取组件实例 `this`
      // 因为当钩子执行前，组件实例还没被创建
      loadScript()
      next(vm => {
        vm.$store.commit('SET_LOADING', true)
        setTimeout(function () {
          initialize()
          vm.$store.commit('SET_LOADING', false)
        }, 1000)
      })
    },
    watch: {
      $route () {
        loadScript()
        this.$store.commit('SET_LOADING', true)
        setTimeout(function () {
          initialize()
          this.$store.commit('SET_LOADING', false)
        }, 1000)
      }
    }
  }
</script>

<style scoped>
.patient-banner {
  height: 150px;
  background-image: url('/static/images/iceland.jpg');
  background-position: center;
  background-size: cover;
}
.aid-avatar {
  width: 100px;
  position: absolute;;
  top: 100px;
  left: 50%;
  margin-left: -50px;
  border-radius: 100%;
  border: 3px solid #fff;
}
.patient-name {
  margin-top: 50px;
  text-align: center;
}
.text-center {
  text-align: center;
}

.text-muted {
  font-size: 10px;
}

.bottom-border {
  padding-top: 10%;
  padding-bottom: 10%;
  border-bottom: 1px solid rgba(0,0,0,.1);
}
.keeper-title {
  align-self: flex-start;
  padding-left: 15px;
  border-left: 5px solid #00897B;
  color: #00897B;
  font-weight: 500;
}
</style>
