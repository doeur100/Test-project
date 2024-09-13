<template>
  <div class="containers">
    <div class="card-item flex flex-row">
      <div class="card-left">
        <div class="icon">
          <span class="material-symbols-outlined"> share </span>
          <span class="material-symbols-outlined"> favorite </span>
        </div>
        <div class="main-img">
          <img src="/apple-red.png" alt="" />
        </div>
        <div class="sub-img">
          <img src="../../assets/image/apple.png" alt="" />
          <img src="../../assets/image/apple.png" alt="" />
          <img src="../../assets/image/apple.png" alt="" />
          <img src="../../assets/image/apple.png" alt="" />
        </div>
      </div>
      <div class="card-right">
        <div style="">
          <h2>Delicious Apples</h2>
          <span>7.93$</span>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.containers {
  display: flex;
  justify-content: center;
  margin-top: 10rem;
}
.card-item {
  background: rgb(244, 37, 78);
  background: linear-gradient(
    41deg,
    rgba(244, 37, 78, 1) 1%,
    rgba(122, 253, 45, 1) 100%
  );
  box-shadow: rgba(100, 100, 111, 0.2) 0px 7px 29px 0px;
  width: 35rem;
  gap: 2rem;
  padding: 2rem;
  align-items: center;
}
.card-left {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  background: rgb(255, 255, 255);
  background: radial-gradient(
    circle,
    rgba(255, 255, 255, 1) 0%,
    rgba(148, 233, 153, 1) 63%
  );
  height: 29rem;
  padding: 1rem;
  border-radius: 10px;
  box-shadow: rgba(0, 0, 0, 0.22) 0px 10px 58px,
    rgba(0, 0, 0, 0.22) 0px 10px 10px;
  margin-left: -8rem;
}
.card-right {
  /* background-color: red; */
  height: 30rem;
  /* width: 35rem; */
}
.main-img img {
  width: 25rem;
  position: absolute;
  margin-left: -7rem;
  margin-top: -8rem;
}
.sub-img img {
  width: 4rem;
  border: 1px solid red;
  margin: 5px;
}
.sub-img {
  display: flex;
}
.icon {
  display: flex;
  justify-content: space-between;
}
</style>
