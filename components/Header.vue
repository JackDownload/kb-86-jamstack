<template>
  <header class="header">
    <section class="header__section section__wrapper">
      <nuxt-link to="/" class="hdr-logo-link" rel="home">
        <span class="screen-reader__text">Ga naar Home</span>
        <Logo />
      </nuxt-link>
      <nav id="nav-main" class="nav--main" role="navigation">
        <ul class="nav__list--main">
          <li class="nav__list-item">
            <nuxt-link to="/" class="nav__link">Home</nuxt-link>
          </li>
          <li class="nav__list-item">
            <nuxt-link to="/blogs" class="nav__link">Blogs</nuxt-link>
          </li>
          <li>
            <a href="https://kb-86.admin.datocms.com/" target="_blank" rel="noreferrer" class="nav__link nav__button">Inloggen</a>
          </li>
        </ul>
      </nav><!-- #nav -->
    </section>
  </header>
</template>

<script>
import Logo from '~/components/Logo.vue';

export default {
  components: {
    Logo
  }
}
</script>
<style lang="scss">
.nav {
  &__list {

    &-item {
      margin-right: 2rem;
    }

    &--main {
      list-style-type: none;
      display: flex;
      align-items: center;
    }
  }

  &__link {
    font-size: 1.4rem;
    text-decoration: none; 
    color: $c-primary;
    display: block;

    &:hover {
      color: $c-secondary;
    }
  }

  &__button {
    padding: .7rem 2rem;
    font-size: 1.2rem;
    border-radius: .3rem;
    background-color: $c-primary;
    color: white;

    &:hover {
      color: white;
      background-color: $c-secondary;
      cursor: pointer;
    }
  }
}

.header {
  top: 0;
  position: sticky;
  z-index: 10;
  background-color: white;
  margin-bottom: 2rem;
  
  &__section {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 120px;
  }

  &--scrolled {
    box-shadow: 0px 2px 4px 0px rgba(0, 0, 0, 0.2);
  }
}
</style>