<template>
  <Teleport to="body">
    <div class="background">
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      <span></span>
    </div>
  </Teleport>
  <header>
    <div class="services-heading">
      <h1 class="background-heading-main">Ukázky mé práce</h1>
      <h1 class="background-heading">Ukázky mé práce</h1>
    </div>
  </header>
  <div class="reference">
    <div class="ref1" data-aos="zoom-in">
      <a href="https://www.bagrychrencik.cz/">
        <div class="ref-content"><h2>Chrenčík dopravní stavby</h2></div>
      </a>
    </div>
    <div class="ref2" data-aos="zoom-in">
      <a href="https://czechwhitediamond.cz/">
        <div class="ref-content"><h2>Czech White Diamond</h2></div>
      </a>
    </div>
    <div class="ref3" data-aos="zoom-in">
      <a href="https://palettenservicelogistik.cz/">
        <div class="ref-content"><h2>Paletten service logistik s.r.o.</h2></div>
      </a>
    </div>
    <div class="ref4" data-aos="zoom-in">
      <a href="https://georgegoaliegear.cz/">
        <div class="ref-content"><h2>George Goalie Gear</h2></div>
      </a>
    </div>
  </div>
  <footer>
    <h2><router-link to="/">Weby PeBa</router-link></h2>
    <h3>Všechna práva vyhrazena © 2024</h3>
  </footer>
</template>

<style scoped>
a {
  text-decoration: none;
  color: var(--main-green);
}
.reference {
  margin: 0 auto;
  width: 90%;
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  gap: 20px;
  justify-content: center;
  padding-bottom: 30px;
}
.ref1,
.ref2,
.ref3,
.ref4 {
  background-size: cover;
  background-position: 50% 50%;
  background-repeat: no-repeat;
  background-position-x: center;
  box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
  height: 450px;
  flex: 0 0 45%;
  box-sizing: border-box;
  position: relative;
  overflow: hidden;
  border-radius: 20px;
  transition: all 0.5s;
}
.ref1 {
  background-image: url(/src/assets/chrenfinal.png);
}
.ref2 {
  background-image: url(/src/assets/czechfinal.png);
}
.ref3 {
  background-image: url(/src/assets/paletfinal.png);
}
.ref4 {
  background-image: url(/src/assets/george.jpg);
}
.ref-content {
  text-align: center;
  display: flex;
  align-items: flex-end;
  justify-content: center;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(
    0deg,
    rgba(0, 0, 0, 0.9) 2%,
    rgba(0, 0, 0, 0) 63%
  );
  transform: translateY(100%);
  transition: all 1s;
}
.ref1:hover .ref-content,
.ref2:hover .ref-content,
.ref3:hover .ref-content,
.ref4:hover .ref-content {
  transform: translateY(0%);
}
.ref-content h2 {
  margin-bottom: 20px;
}
.ref1:hover,
.ref2:hover,
.ref3:hover,
.ref4:hover {
  transform: scale(1.05);
  transition: all 1s;
  z-index: 20;
}
.ref img {
}

@media screen and (max-width: 1000px) {
  .reference {
    flex-direction: column;
  }
  .ref-content {
    transform: translateY(0%);
  }
  .ref1,
  .ref2,
  .ref3,
  .ref4 {
    flex: none;
    height: 350px;
    width: 90%;
  }
  .ref1:hover,
  .ref2:hover,
  .ref3:hover,
  .ref4:hover {
    transform: scale(1.1);
  }
}
</style>
