<template>
  <nav class="main-nav">
    <div class="logo">
      <a href="/"> <h3>Weby PeBa</h3></a>
    </div>
    <div class="nav-links">
      <router-link to="/">Domů</router-link>
      <span class="quote">|</span>
      <router-link to="/sale">Hotové designy k prodeji</router-link>
      <span class="quote">|</span>
      <router-link to="/about">Reference</router-link>
      <span class="quote">|</span>
      <router-link to="/price">Ceník</router-link>
      <span class="quote">|</span>
      <router-link to="/contact">Kontakt</router-link>
    </div>
  </nav>

  <nav class="nav-hamburger">
    <div class="logo">
      <h3>Weby PeBa</h3>
    </div>
    <transition name="menu">
      <div class="nav-links" v-if="hamburgerShow">
        <router-link to="/" @click="hamburgerShow = false">Domů</router-link>
        <span class="quote">|</span>
        <router-link to="/sale" @click="hamburgerShow = false"
          >Hotové designy k prodeji</router-link
        >
        <span class="quote">|</span>
        <router-link to="/about" @click="hamburgerShow = false"
          >Reference</router-link
        >
        <span class="quote">|</span>
        <router-link to="/price" @click="hamburgerShow = false"
          >Ceník</router-link
        >
        <span class="quote">|</span>
        <router-link to="/contact" @click="hamburgerShow = false"
          >Kontakt</router-link
        >
      </div>
    </transition>
    <div class="demo" @click="toggleHamburgerShow">
      <div class="menu-icon">
        <input class="menu-icon__cheeckbox" type="checkbox" />
        <div>
          <span></span>
          <span></span>
        </div>
      </div>
    </div>
  </nav>
  <router-view />
</template>

<script>
import { reactive, toRefs } from "vue";

export default {
  setup() {
    const state = reactive({
      hamburgerShow: false,
    });
    const toggleHamburgerShow = () => {
      state.hamburgerShow = !state.hamburgerShow;
    };

    return {
      ...toRefs(state),
      toggleHamburgerShow,
    };
  },
};
</script>

<style>
#app {
  font-family: var(--heading-font);
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: var(--main-green);
}
body {
  background-color: var(--main-black);
}

nav {
  padding: 30px;
  width: 100%;
  display: flex;
  gap: 1rem;
  box-sizing: border-box;
  justify-content: space-between;
}
.logo h3 {
  color: var(--main-green);
}
.nav-hamburger {
  display: none;
}
nav a {
  font-weight: bold;
  color: var(--main-white);
  text-decoration: none;
}
a.router-link-exact-active {
  color: var(--main-gold);
  text-decoration: underline;
}
nav .nav-links {
  display: flex;
  gap: 1rem;
  text-transform: uppercase;
}
.main-nav {
  z-index: 10;
  position: relative;
}
/* HAMBURGER */
.hamburger {
  position: relative;
}
.center {
  padding-top: 30px;
  padding-right: 30px;
  transform: translate(-50%, -50%);
  position: absolute;
  width: 50px;
}

.center:before,
.center:after,
.center div {
  background: #fff;
  content: "";
  display: block;
  height: 6px;
  border-radius: 3px;
  margin: 7px 0;
  transition: 0.5s;
}
.center:active:before {
  transform: translateY(12px) rotate(135deg);
}
.center:active:after {
  transform: translateY(-12px) rotate(-135deg);
}
.center:active div {
  transform: scale(0);
}
/* Transition */
.menu-enter-active,
.menu-leave-active {
  transition: opacity 0.5s;
}
.menu-enter,
.menu-leave-to {
  opacity: 0;
}
@media screen and (max-width: 900px) {
  .logo {
    display: flex;
    align-items: center;
  }
  .main-nav {
    display: none;
  }
  .nav-hamburger {
    position: relative;
    display: flex;
  }
  .nav-links {
    background-color: var(--main-black);
    display: flex;
    flex-direction: column;
    align-items: center;
    /* height: 100px; */
    position: fixed;
    padding-bottom: 30px;
    left: 0;
    top: 0;
    padding-top: 100px;
    width: 100%;
    z-index: 3;
  }
  .quote {
    display: none;
  }
  .header-text {
    padding-left: 0px;
  }
}
</style>
<style lang="scss">
.demo {
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 4;
  // 	for demo
  .menu-icon {
    transform: scale(1.5);
  }
}

:root {
  --bar-bg: #32393f;
}

.menu-icon {
  position: relative;
  width: 50px;
  height: 50px;
  cursor: pointer;

  .menu-icon__cheeckbox {
    display: block;
    width: 100%;
    height: 100%;
    position: relative;
    cursor: pointer;
    z-index: 2;
    -webkit-touch-callout: none;
    position: absolute;
    opacity: 0;
  }
  div {
    margin: auto;
    position: absolute;
    top: 0;
    right: 0;
    left: 0;
    bottom: 0;
    width: 22px;
    height: 12px;
  }
  span {
    position: absolute;
    display: block;
    width: 100%;
    height: 2px;
    background-color: var(--bar-bg, #000);
    border-radius: 1px;
    transition: all 0.2s cubic-bezier(0.1, 0.82, 0.76, 0.965);

    &:first-of-type {
      top: 0;
    }
    &:last-of-type {
      bottom: 0;
    }
  }
  &.active,
  .menu-icon__cheeckbox:checked + div {
    span {
      &:first-of-type {
        transform: rotate(45deg);
        top: 5px;
      }
      &:last-of-type {
        transform: rotate(-45deg);
        bottom: 5px;
      }
    }
  }

  &.active:hover span:first-of-type,
  &.active:hover span:last-of-type,
  &:hover .menu-icon__cheeckbox:checked + div span:first-of-type,
  &:hover .menu-icon__cheeckbox:checked + div span:last-of-type {
    width: 22px;
  }

  &:hover {
    // no need hover effect on mobile.
    @media (min-width: 1024px) {
      span:first-of-type {
        width: 26px;
      }

      span:last-of-type {
        width: 12px;
      }
    }
  }
}
</style>
