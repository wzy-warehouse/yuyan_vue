<template>
  <div class="disaster-container">
    <div class="title">
      <div class="title-content">
        <img src="@/assets/images/titleLeft.png" alt="title left" />
        <span class="title-span">灾害<span class="title-blue">应急</span></span>
        <img src="@/assets/images/titleRight.png" alt="title right" />
      </div>
    </div>
    <div class="disaster-map">
      <ul>
        <li class="map">
          <a href="/disaster1" target="_blank">
            <img src="/images/disaster/disaster-1-cover.png" alt>
          </a>
          <p class="map-info">西藏定日6.8级地震应急监测评估</p>
          <p class="time">2025-01-17</p>
        </li>
        <li class="map">
          <a href="/disaster2" target="_blank">
            <img src="/images/disaster/disaster-2-cover.png" alt>
          </a>
          <p class="map-info">四川筠连山体滑坡应急监测评估</p>
          <p class="time">2025-02-10</p>
        </li>
        <li class="map">
          <a href="/disaster3" target="_blank">
            <img src="/images/disaster/disaster-3-cover.png" alt>
          </a>
          <p class="map-info">云南福贡县亚目水电站滑坡应急监测</p>
          <p class="time">2025-03-22</p>
        </li>
        <li class="map">
          <a href="/disaster4" target="_blank">
            <img src="/images/disaster/disaster-4-cover.png" alt>
          </a>
          <p class="map-info">贵州大方县果瓦乡山体滑坡无人机应急监测</p>
          <p class="time">2025-05-26</p>
        </li>
        <li class="map">
          <a href="/disaster5" target="_blank">
            <img src="/images/disaster/disaster-4-cover.png" alt>
          </a>
          <p class="map-info">山东济南市莱芜区大王庄镇山洪无人机应急监测</p>
          <p class="time">2025-07-31</p>
        </li>
      </ul>
      <div class="disaster-more">查看更多</div>
    </div>
  </div>
</template>

<script setup>

</script>

<style scoped>
.title {
  width: 100%;
  max-width: 1200px;
  height: 50px;
  margin: 40px auto;
  font-size: 36px;
  color: #333;
  line-height: 50px;
  text-align: center;
  position: relative;
}

.title-content {
  width: 100%;
  margin: 0 auto;
}

.title-content img {
  margin-bottom: 5px;
}

.title-content .title-span {
  font-family: PingFangSC, PingFang SC;
  font-weight: 600;
  margin: 0 50px;
}

.title-blue {
  color: #3F93DA;
}

.disaster-map{
  width: 100%;
}

.disaster-map ul{
  overflow: hidden;
}

.disaster-map .map{
  float: left;
  width: 18%;
  height: 280px;
  margin-left: 1%;
  margin-bottom: 15px;
}

.disaster-map .map a{
  display: block;
  width: 100%;
  height: 200px;
}

.disaster-map .map a>img{
  width: 100%;
  height: 100%;
}

.disaster-map .map .map-info{
  font-size: 14px;
  color: #333;
  margin-bottom: 0;
  margin-top: 5px;
}

.disaster-map .map .time{
  font-size: 12px;
  color: #999999;
  margin-bottom: 0;
}

.disaster-more{
  color: #999999;
  position: absolute;
  right: 20%;
}
</style>