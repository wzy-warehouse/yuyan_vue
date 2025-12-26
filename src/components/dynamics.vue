<template>
  <div class="dynamics-container">
    <div class="title">
      <div class="title-content">
        <img src="@/assets/images/titleLeft.png" alt="title left" />
        <span class="title-span">机制<span class="title-blue">动态</span></span>
        <img src="@/assets/images/titleRight.png" alt="title right" />
      </div>
    </div>
    <div class="dynamics-list">
      <ul>
        <li class="dynamics-item">
          <router-link to="/dynamic1">20250109-"重大灾害无人机应急合作机制"业务交流和技术研讨会在哈尔滨召开</router-link>
        </li>
        <li class="dynamics-item">
          <router-link to="/dynamic2">20250307-机制动态："重大灾害无人机应急合作机制"2025年考核和增补工作圆满完成</router-link>
        </li>
        <li class="dynamics-item">
          <router-link to="/dynamic3">20250326-机制动态：聚青年英才之力 筑无人机应急防线</router-link>
        </li>
        <li class="dynamics-item">
          <router-link to="/dynamic4">20250426-机制动态："雨燕应急"2025首期线上培训圆满完成，684名无人机应急尖兵云端集结</router-link>
        </li>
        <li class="dynamics-item">
          <router-link to="/dynamic5">20250530-业务交流：国家减灾中心派员参加2025第九届世界无人机大会暨UASE无人机展</router-link>
        </li>
      </ul>
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

.dynamics-list {
  max-width: 1200px;
  padding: 20px;
}

.dynamics-item {
  padding: 10px 0;
  border-bottom: 1px solid #eee;
  list-style: none;
}

.dynamics-item:last-child {
  border-bottom: none;
}

.dynamics-item a {
  display: block;
  padding: 10px;
  text-decoration: none;
  color: #333;
  transition: background-color 0.3s;
  border-radius: 4px;
}

.dynamics-item a:hover {
  background-color: #f5f5f5;
  color: #3F93DA;
}
</style>