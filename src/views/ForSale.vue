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
  <div class="services-heading">
    <h1 class="background-heading-main">Hotové designy k prodeji</h1>
    <h1 class="background-heading">Hotové designy k prodeji</h1>
  </div>
  <div class="container">
    <div class="done-box box1">
      <a href="https://coffee.weby-peba.cz/" class="photo"></a>
      <div class="text">
        <h1>Coffee</h1>
        <p>
          Představuji unikátní design inspirovaný atmosférou útulné kavárny –
          ideální pro všechny, kteří chtějí svým webovým stránkám či projektu
          dodat teplo, styl a špetku kofeinového šarmu. Elegantní detaily,
          zemitá paleta barev a motivy spojené s kávou zaručí, že váš web osloví
          nejen milovníky kávy, ale každého, kdo ocení kvalitní design s duší.
          Váš projekt, vaše káva – s designem, který probudí smysly!
        </p>
        <a
          href="mailto:info@weby-peba.cz?subject=Dotaz%20na%20šablonu%20Coffee&body=Dobrý%20den,%0A%0Amám%20zájem%20o%20šblonu%20Coffee.%20Můžete%20mi%20poskytnout%20další%20informace?&bcc=pebaweby@gmail.com"
          ><button class="demand">Mám zájem!</button></a
        >
      </div>
    </div>
    <div class="done-box box2">
      <a href="https://detailing.weby-peba.cz/" class="photo"></a>
      <div class="text">
        <h1>Detailing</h1>
        <p>
          Přináším Vám design inspirovaný světem profesionálního detailingu –
          čistý, precizní a dokonale vyladěný. Tento moderní a elegantní styl je
          ideální pro weby, které chtějí svým zákazníkům ukázat, že jejich
          vozidla dostanou péči až do posledního detailu. Lesk, elegance a výkon
          – váš web bude odrazem špičkové kvality služeb, které nabízíte.
          Posuňte svůj byznys o úroveň výš s designem, který září stejně jako
          čerstvě ošetřený vůz!
        </p>
        <a
          href="mailto:info@weby-peba.cz?subject=Dotaz%20na%20šablonu%20Detailing&body=Dobrý%20den,%0A%0Amám%20zájem%20o%20šablonu%20Detailing.%20Můžete%20mi%20poskytnout%20další%20informace?&bcc=pebaweby@gmail.com"
          ><button class="demand">Mám zájem!</button></a
        >
      </div>
    </div>
  </div>
  <footer>
    <h2><router-link to="/">Weby PeBa</router-link></h2>
    <h3>Všechna práva vyhrazena © 2024</h3>
  </footer>
</template>
<style scoped>
.background-heading {
  color: var(--main-black);
  -webkit-text-stroke: 2px var(--main-green);
  opacity: 0.2;
  font-size: clamp(3rem, 2.6429rem + 1.6vw, 4.05rem);
  position: absolute;
  bottom: 0px;
  text-transform: uppercase;
}
.background-heading-main {
  z-index: 2;
  position: relative;
  text-transform: uppercase;
}
.services-heading {
  position: relative;
  padding-left: 10vw;
  padding-top: 30px;
  margin-bottom: 30px;
}
.container {
  display: flex;
  gap: 20px;
  flex-direction: column;
  margin: 0 auto;
  width: 80%;
  padding-bottom: 10vw;
}
.done-box {
  display: flex;
  box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
  border-radius: 20px;
}
.done-box .photo {
  background-size: cover;
  width: 50%;
  height: 350px;
  transition: all 0.5s;
  border-radius: 20px 0 0 20px;
  background-position: 50% 50%;
}
.done-box .text {
  width: 50%;
  padding: 20px 40px 20px 40px;
  color: var(--light-green);
}
.done-box .text h3 {
  font-size: 1.5rem;
}
.box1 .photo {
  background-image: url(/src/assets/caffe-screen.jpg);
}
.box2 .photo {
  background-image: url(/src/assets/detailing-screen.jpg);
}
.done-box .photo:hover {
  transform: scale(1.05);
  cursor: pointer;
}
p {
  color: #f8f8f8;
  font-size: 16px;
  font-weight: 200;
}

@media screen and (max-width: 1000px) {
  .done-box {
    flex-direction: column-reverse;
    margin-top: 30px;
  }
  .done-box .photo,
  .done-box .text {
    width: 100%;
  }
  .done-box .photo {
    border-radius: 20px;
  }
  .container {
    width: 95%;
  }
}
</style>
