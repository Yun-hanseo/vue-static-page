<template>
  <div class="chuseok-wrapper">
    <div class="moon"></div>
    <div class="cloud cloud1"></div>
    <div class="cloud cloud2"></div>

    <div class="greeting">
      <h1>🌕 행복한 한가위 되세요 🌾</h1>
      <p>가족과 함께하는 따뜻한 시간 보내세요 🍁</p>
    </div>

    <div class="ground"></div>
  </div>
</template>

<script setup lang="ts">
// 단순 정적 한가위 페이지
</script>

<style scoped>
/* ✅ 브라우저 전체를 강제로 채움 */
html, body, #app {
  width: 100%;
  height: 100%;
  margin: 0;
  padding: 0;
}

.chuseok-wrapper {
  width: 100vw;
  height: 100vh;
  overflow: hidden;
  position: relative;
  background: linear-gradient(to top, #2c3e50, #f0c27b);
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

/* 🌕 달 */
.moon {
  position: absolute;
  top: 15%;
  left: 50%;
  transform: translateX(-50%);
  width: 20vmin;
  height: 20vmin;
  background: radial-gradient(circle at 30% 30%, #fff8dc, #f6e58d, #f0c27b);
  border-radius: 50%;
  box-shadow: 0 0 80px rgba(255, 255, 200, 0.8);
  animation: float 6s ease-in-out infinite;
}

/* ☁️ 구름 */
.cloud {
  position: absolute;
  background: rgba(255, 255, 255, 0.7);
  border-radius: 50%;
  opacity: 0.8;
  filter: blur(4px);
  animation: moveClouds 45s linear infinite;
}

.cloud1 {
  width: 25vmin;
  height: 8vmin;
  top: 25%;
  left: -25vmin;
  animation-delay: 0s;
}

.cloud2 {
  width: 20vmin;
  height: 6vmin;
  top: 40%;
  left: -40vmin;
  animation-delay: 10s;
}

@keyframes moveClouds {
  from { transform: translateX(0); }
  to { transform: translateX(130vw); }
}

@keyframes float {
  0%, 100% { transform: translate(-50%, 0); }
  50% { transform: translate(-50%, -10px); }
}

/* 🎑 문구 */
.greeting {
  position: relative;
  z-index: 3;
  color: #fff;
  text-align: center;
  text-shadow: 0 2px 10px rgba(0, 0, 0, 0.5);
  margin-top: 25vmin;
}

.greeting h1 {
  font-size: 4vmin;
  font-family: 'Pretendard', 'Noto Sans KR', sans-serif;
}

.greeting p {
  font-size: 2vmin;
  margin-top: 1rem;
  opacity: 0.9;
}

/* 🌾 바닥 */
.ground {
  position: absolute;
  bottom: 0;
  width: 100%;
  height: 15vmin;
  background: linear-gradient(to top, #3e2723, #8d6e63);
}
</style>



