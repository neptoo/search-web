<template>
  <div class="home">
    <svg t="1583663700282" class="icon-logo" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="3188" width="200" height="200"><path d="M382.933333 274.944c75.221333 121.173333 128.426667 226.176 168.618667 324.992a1541.12 1541.12 0 0 1-62.634667 196.608c-26.368-104.618667-52.992-202.624-112-297.002667 13.013333-72.789333 4.608-147.2 6.016-224.597333z" fill="#FFC107" p-id="3189"></path><path d="M287.914667 421.333333H101.546667c-13.013333 0-20.992 15.018667-13.013334 25.386667 84.394667 108.629333 143.36 235.605333 183.381334 374.613333h207.018666c-32.426667-139.392-77.397333-267.392-164.992-386.986666a33.152 33.152 0 0 0-26.026666-13.013334z" fill="#4CAF50" p-id="3190"></path><path d="M383.573333 245.333333c136.96 216.021333 259.968 468.992 276.352 736h227.413334c-24.021333-276.010667-136.789333-530.005333-286.421334-736H383.573333z" fill="#FF3D00" p-id="3191"></path><path d="M887.125333 108.373333A31.488 31.488 0 0 0 856.746667 85.333333h-176.64c-10.581333 0-17.962667 9.984-15.573334 20.608a1537.28 1537.28 0 0 1 52.992 292.010667c96.426667 172.373333 159.402667 356.565333 181.205334 541.568 31.573333-121.002667 50.602667-267.008 50.602666-405.973333 0-147.2-24.192-290.218667-62.208-425.216z" fill="#1976D2" p-id="3192"></path></svg>
    <div class="home-search-panel">
      <SearchLogo class="search-logo" />
      <HomeSearchBar class="home-search-bar" />
    </div>
  </div>
</template>

<script>
import SearchLogo from "@/components/SearchLogo.vue";
import HomeSearchBar from "@/components/HomeSearchBar.vue";

export default {
  name: "Home",
  components: {
    SearchLogo,
    HomeSearchBar
  }
};
</script>
<style lang="less">
.search-logo {
  margin-top: 30px;
  margin-bottom: 30px;
}
.home-search-bar {
  max-width: 650px;
  margin: 0 auto;
}
.icon-logo {
  width: 9rem;
  height: 10rem;
  vertical-align: middle;
  fill: currentColor;
  overflow: hidden;
  margin-top: 80px;
}
</style>
