<script setup lang="ts"></script>

<template>
  <div class="card">
    <div class="front">
      <img src="" alt="" />
    </div>
    <div class="back">
      <h1>
        John Doe
        <span>Software Engineer</span>
      </h1>
      <ul class="socials">
        <li>
          <a href=""></a>
        </li>
        <li>
          <a href=""></a>
        </li>
        <li>
          <a href=""></a>
        </li>
      </ul>
    </div>
  </div>
</template>

<style scoped>
.wrapper {
  background-color: beige;
  height: 100vh;
}

.card {
  width: 340px;
  height: 480px;
  cursor: pointer;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);

  &:hover {
    .back {
      transform: perspective(600px) rotateY(0);
    }

    .front {
      transform: perspective(600px) rotateY(-180deg);
    }
  }
}

.front,
.back {
  width: 100%;
  height: 100%;
  overflow: hidden;
  backface-visibility: hidden;
  -webkit-backface-visibility: hidden;
  position: absolute;
  transition: transform 0.5s ease;
  border-radius: 10px;
  background: linear-gradient(#d6d6d6, #f2f2f2);
}

.front {
  transform: perspective(600px) rotateY(0);
}

.back {
  transform: perspective(600px) rotateY(180deg);
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
}

.back h1 {
  color: #444;
  font-size: 24px;
}

.back h1 span {
  display: block;
  font-size: 18px;
  font-weight: 300;
  margin: 5px 0 10px;
}
</style>
