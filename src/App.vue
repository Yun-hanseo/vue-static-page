<template>
  <div class="chuseok-page">
    <!-- 🌕 달 -->
    <div class="moon"></div>

    <!-- ☁️ 구름 -->
    <div class="cloud cloud1"></div>
    <div class="cloud cloud2"></div>

    <!-- 🎑 한가위 인사 -->
    <div class="greeting">
      <h1>🌕 행복한 한가위 되세요 🌾</h1>
      <p>가족과 함께하는 따뜻한 시간 보내세요 🍁</p>
    </div>

    <!-- 🎵 바닥 장식 -->
    <div class="ground"></div>
  </div>
</template>

<script setup lang="ts">
// 특별한 로직은 없음, 순수히 디자인용 페이지
</script>

<style scoped>
/* 전체화면 기본 설정 */
html, body, #app, .chuseok-page {
  width: 100%;
  height: 100%;
  margin: 0;
  padding: 0;
}

/* 전체 페이지 스타일 */
.chuseok-page {
  position: relative;
  overflow: hidden;
  background: linear-gradient(to top, #2c3e50, #f0c27b);
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

/* 🌕 달 */
.moon {
  position: absolute;
  top: 12%;
  left: 50%;
  transform: translateX(-50%);
  width: 22vmin;
  height: 22vmin;
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
  animation: moveClouds 40s linear infinite;
}

.cloud1 {
  width: 25vmin;
  height: 8vmin;
  top: 30%;
  left: -30vmin;
  animation-delay: 0s;
}

.cloud2 {
  width: 20vmin;
  height: 6vmin;
  top: 45%;
  left: -40vmin;
  animation-delay: 10s;
}

/* ☁️ 구름 이동 */
@keyframes moveClouds {
  from {
    transform: translateX(0);
  }
  to {
    transform: translateX(140vw);
  }
}

/* 🌕 달 살짝 뜨는 애니메이션 */
@keyframes float {
  0%, 100% {
    transform: translate(-50%, 0);
  }
  50% {
    transform: translate(-50%, -10px);
  }
}

/* 🎑 인사 문구 */
.greeting {
  position: relative;
  z-index: 2;
  color: #fff;
  text-align: center;
  text-shadow: 0 2px 10px rgba(0, 0, 0, 0.4);
  margin-top: 30vmin;
  padding: 0 2rem;
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

/* 🌾 바닥 부분 */
.ground {
  position: absolute;
  bottom: 0;
  width: 100%;
  height: 15vmin;
  background: linear-gradient(to top, #3e2723, #8d6e63);
}
</style>


