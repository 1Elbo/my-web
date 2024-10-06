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
  <div class="contact-header">
    <div class="services-heading">
      <h1 class="background-heading-main">Kontakt</h1>
      <h1 class="background-heading">Kontakt</h1>
    </div>
  </div>
  <section class="main">
    <h2>Telefon:</h2>
    <h3><a href="tel:++420776213755">+420 776 213 755</a></h3>
    <h2>Email:</h2>
    <h3><a href="mailto:info@weby-peba.cz">info@weby-peba.cz</a></h3>
    <div class="socials">
      <div class="icon">
        <a
          href="https://www.facebook.com/people/Weby-PeBa/61560849421859/?_rdr"
        >
          <img
            src="@/assets/facebook.png"
            alt="web-icon"
            width="45px"
            height="45px"
          />
        </a>
      </div>
      <div class="icon">
        <a href="https://www.instagram.com/weby_peba/">
          <img
            src="@/assets/instagram.png"
            alt="web-icon"
            width="45px"
            height="45px"
          />
        </a>
      </div>
    </div>
  </section>
  <footer>
    <h2><router-link to="/">Weby PeBa</router-link></h2>
    <h3>Všechna práva vyhrazena © 2024</h3>
  </footer>
</template>

<style scoped>
.contact-header {
  width: 50%;
}
.contact-header h1 {
  text-transform: uppercase;
}
.main {
  background-color: var(--secondary-black);
  box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
  width: 30%;
  margin-left: 10vw;
  padding: 20px;
}
.main h3 {
  margin-left: 20px;
  font-size: 1.2rem;
}
.main h3 a {
  text-decoration: none;
  color: #f8f8f8;
}
h2 {
  font-size: 2rem;
}
.socials {
  display: flex;
}
.icon {
  padding-right: 20px;
  padding-top: 20px;
}
.icon a img:hover {
  transform: scale(1.1);
}
footer {
  position: fixed;
  bottom: 0;
}
.footer a {
  color: var(--main-green) !important;
}
@media screen and (max-width: 980px) {
  .main {
    width: 80%;
  }
}
</style>
