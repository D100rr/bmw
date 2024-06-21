<script setup>
const links = [
  { title: "BMW", route: "/" },
  { title: "AUDI", route: "/" },
  { title: "FERRARI", route: "/" },
  { title: "PORSCHE", route: "/" },
]
</script>

<template>
  <header class="header">
    <nav class="header__nav">
      <div class="header__nav-content container">
        <h1 class="header__nav-title">
          ELITE
        </h1>
        <ul class="header__nav-list">
          <li class="header__nav-item" v-for="link of links" :key="link.title">
            <router-link :to="link.route" class="header__nav-link">{{ link.title }}</router-link>
          </li>
        </ul>
        <form class="header__nav-form">
          <input type="text" placeholder="Search..">
          <i class="icon pi pi-search"></i>
        </form>
      </div>
    </nav>
    <div class="header__bg-img">
      <img src="@/assets/img/bmw header.png" alt="" class="header__bg-img">
    </div>
  </header>
</template>

<style lang="scss" scoped>
.header {
  height: 100vh;
  display: flex;
  flex-direction: column;

  &__nav {
    background: #625451;
    padding: 10px 0;

    &-content {
      display: flex;
      align-items: center;
      justify-content: space-between;
    }

    &-title {
      font-size: 48px;
      color: #FFFFFF;
      font-weight: 700;
      line-height: 48px;

    }

    &-list {
      display: flex;
      align-items: center;
      gap: 30px;
    }

    &-link {
      font-size: 20px;
      font-weight: 500;
      color: #FFFFFF;
    }

    &-form {
      background: #DEC3B8;
      padding: 1px;
      display: flex;
      align-items: center;

      & input {
        background: none;
        border: none;
        outline: none;
        padding: 0 5px;

        &::placeholder {
          color: #FFFFFF;
        }
      }

      & i {
        font-size: 18px;
        color: #FFFFFF;
        background: #B28C7D;
        padding: 3px;
        border-radius: 1px;
      }
    }

  }

  .header__bg-img {
    flex-grow: 1;
  }

  .header__bg-img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }

}
</style>