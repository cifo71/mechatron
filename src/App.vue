<template>
  <div id="app">
    <header class="header">
      <router-link :to="{ name: 'home' }">
        <img src="@/assets/img/logo2.png" />
      </router-link>
      <nav>
        <a href="#home">Domov</a>
        <a href="#about">O nás</a>
        <a href="#services">Naše služby</a>
        <a href="#contact">Kontaktujte nás</a>
      </nav>
    </header>

    <section>
      <router-view/>
    </section>

    <footer class="footer">
      <p>Copyright &copy; 2018, Designed by chnapkor.</p>
    </footer>
  </div>
</template>

<style lang="scss">
@import "~@/assets/scss/reset";
@import "~@/assets/scss/variables";
@import "~@/assets/scss/mixins";

.header {
  width:           100%;
  height:          80px;
  background:      $black;
  padding:         0 40px;
  display:         flex;
  align-items:     center;
  justify-content: space-between;
  position:        fixed;
  top:             0;
  left:            0;

  img {
    max-width: 100px;
  }

  nav {
    display: none;
    @include media(md) {
      display: flex;
    }

    a {
      padding:   12px;
      color:     $accent;
      font-size: 18px;
      display:   block;

      &:not(:last-of-type) {
        margin-right: 60px;
      }
      
      &:hover {
        color: $primary;
      }
    }
  }
}

.footer {
    position: fixed;
    left: 0;
    bottom: 0;
    width: 100%;
    background-color: black;
    color: white;
    text-align: center;
}
</style>
