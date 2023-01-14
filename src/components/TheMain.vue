<template>
  <main>
    <div class="container">
      <div class="banner__img">
        <img src="../assets/techhub.png" alt="" />
      </div>
      <h1>👨‍💻 «TechHub» oʻquv markazi oʻz faoliyatini boshladi</h1>
    </div>
  </main>
</template>
  
  
  <script>
export default {
  name: "TheMain",
};
</script>
  
<style lang="scss" scoped>
main {
  width: 100%;
  height: 100vh;
  position: absolute;
  top: 0;
  z-index: 1;
  background: url(../assets/banner1.jpg);
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  display: flex;
}

.container 
  // display: flex;
  // flex-direction: column;
  // justify-content: center;
  // align-items: center;
  // gap: 30px;
  // h1 {
  //   color: white;
  //   text-shadow: 0 0 15px #fff, 0 0 30px rgb(75, 255, 26), 0 0 75px #49ff18,
  //     27px -9px 15px rgba(206, 89, 55, 0);
  // }
}

.banner__img {
  display: flex;
  justify-content: center;
  align-content: flex-end;
  width: 350px;
  height: 350px;
  padding: 10px 20px;
  background: rgba(255, 215, 0, 0.9);
  box-shadow: 7px 8px 25px 2px rgba(75, 255, 26, 0.6);
  backdrop-filter: blur(1px);
  -webkit-backdrop-filter: blur(1px);
  border-radius: 20px;
  border: 1px solid rgba(255, 255, 255, 0.18);
}
</style>