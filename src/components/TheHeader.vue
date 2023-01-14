<template>
  <div class="filter" :class="{ active: this.class }" @click="this.class = false"></div>
  <header>
    <div class="container">
      <div class="logo">
        <a href="#">
          <span>Tech</span>
          <span>Hub</span>
        </a>
      </div>
      <nav>
        <ul class="nav__ul" :class="{ active: this.class }">
          <div class="exit" @click="this.class = false">
            <div class="my-button">
              <div class="btn-elem"></div>
            </div>
          </div>
          <ul class="items">
            <li><a href="#">Home</a></li>
            <li><a href="#">Page 5</a></li>
            <li><a href="#">Page 6</a></li>
            <li><a href="#">Page 7</a></li>
          </ul>
        </ul>
        <div class="button__box" @click="this.class = !this.class">
          <div class="my-button">
            <div class="btn-elem"></div>
          </div>
        </div>
      </nav>
    </div>
  </header>
</template>


<script>
export default {
  name: "TheHeader",
  data(){
    return {
      class: false
    }
  }
};
</script>


<style lang="scss" scoped>

header {
  position: relative;
  z-index: 2;
  background: rgba(255, 215, 0, 0.8);
box-shadow: 0 8px 32px 0 rgba( 31, 38, 135, 2 );
backdrop-filter: blur( 1px );
-webkit-backdrop-filter: blur( 1px );
  padding: 10px 0px;
  border-bottom: 2px dashed #398c16;
}

.container {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.filter.active {
    position: fixed;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    z-index: 10;
    background: rgba(0, 0, 0, 0.9);
}

.logo {
  font-size: 28px;
  line-height: 30px;
  a {
    display: flex;
    font-weight: 600;
    span:first-child {
      color: black;
    }
    span:last-child {
      color: #1b440c;
    }
  }
}

nav {
  .nav__ul {
    @media (max-width: 768px) {
      gap: 18px;
      background: rgba(0, 0, 0, 0.6);
      position: absolute;
      z-index: 11;
      height: 100vh;
      padding: 15px;
      left: -100%;
      top: 0;
      width: 100%;
      max-width: 50vw;
      transition: 2s;
    }
    @media (max-width: 400px) {
      max-width: 70vw;
    }
    .items {
      width: 100%;
      display: flex;
      gap: 24px;
      align-items: center;
      @media (max-width: 768px) {
        margin-top: 20px;
        flex-direction: column;
      }
    }
    a {
      color: black;
      font-weight: 500;
      transition: 0.3s;
      @media (max-width: 768px) {
        font-size: 24px;
        color: rgb(176, 176, 176);
      }
    }
    a:hover {
      color: #398c16;
    }
  }
  .nav__ul.active {
    left: 0;
    -webkit-transition: 0.8s;
    -moz-transition: 0.8s;
    -o-transition: 0.8s;
    transition: 0.8s;
  }
}

.button__box {
  display: none;
  justify-content: center;
  align-items: center;
  width: 40px;
  height: 40px;
  @media (max-width: 768px) {
    display: flex;
  }
  cursor: pointer;
  .my-button {
    display: flex;
    align-items: center;
    justify-content: center;
    .btn-elem {
      position: relative;
      width: 22px;
      border-radius: 8px;
      height: 4px;
      background: #000;
    }
    .btn-elem::before {
      position: absolute;
      border-radius: 8px;
      content: "";
      display: block;
      width: 30px;
      height: 4px;
      top: -11px;
      background: #000;
    }
    .btn-elem::after {
      position: absolute;
      border-radius: 8px;
      content: "";
      display: block;
      width: 30px;
      height: 4px;
      top: 11px;
      background: #000;
    }
  }
}

.button__box:hover .btn-elem {
  width: 30px;
  transition: 0.2s;
  background: #398c16;
}
.button__box:hover .btn-elem::before {
  transition: 0.2s;
  background: #1b440c;
}
.button__box:hover .btn-elem::after {
  transition: 0.2s;
  background: #1b440c;
}

.exit {
  display: none;
  justify-content: end;
  align-items: center;
  width: 100%;
  @media (max-width: 768px) {
    display: flex;
  }
  .my-button {
    cursor: pointer;
    width: 40px;
    height: 40px;
    display: flex;
    align-items: center;
    justify-content: center;
    .btn-elem {
      position: relative;
      width: 32px;
      border-radius: 8px;
      height: 3px;
      background: transparent;
    }
    .btn-elem::before {
      transform: rotate(45deg);
      position: absolute;
      content: "";
      display: block;
      width: 32px;
      border-radius: 8px;
      height: 3px;
      top: 0;
      background: #f7df65;
    }
    .btn-elem::after {
      transform: rotate(-45deg);
      position: absolute;
      content: "";
      display: block;
      border-radius: 8px;
      width: 32px;
      height: 3px;
      top: 0;
      background: #f7df65
    }
  }
}
</style>