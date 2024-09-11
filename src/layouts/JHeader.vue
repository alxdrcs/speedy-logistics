<script setup lang="ts">
import JButton from '~/components/JButton.vue';
</script>

<template>
  <header>
    <div class="container">
      <NuxtLink to="/" class="logo">
        <img src="@/assets/images/logo.png" alt="JH-speedy">
      </NuxtLink>
      <nav>
        <ul>
          <li class="menu-item"><NuxtLink to="/">home</NuxtLink></li>
          <li class="menu-item">
            <NuxtLink to="/">services</NuxtLink>
            <i />
            <ol>
              <li class="sub-item">
                <NuxtLink to="/">sea freight</NuxtLink>
              </li>
              <li class="sub-item">
                <NuxtLink to="/">air freight</NuxtLink>
              </li>
              <li class="sub-item">
                <NuxtLink to="/">express freight</NuxtLink>
              </li>
              <li class="sub-item">
                <NuxtLink to="/">rail freight</NuxtLink>
              </li>
            </ol>
          </li>
          <li class="menu-item">
            <NuxtLink to="/">shipping</NuxtLink>
            <i />
          </li>
          <li class="menu-item">
            <NuxtLink to="/">news</NuxtLink>
            <i />
          </li>
          <li class="menu-item"><NuxtLink to="/">about</NuxtLink></li>
          <li class="menu-item"><NuxtLink to="/">contact</NuxtLink></li>
        </ul>
      </nav>
      <JButton>request a qoute</JButton>
    </div>
  </header>
</template>

<style lang="scss" scoped>
header {
  position: sticky;
  left: 0;
  top: 0;
  width: 100%;
  background-color: #fff;
  padding-top: 10px;

  .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 1240px;
    height: 100px;
    margin: auto;

    .logo {
      img {
        width: 80px;
      }
    }

    nav>ul {
      display: flex;

      .menu-item {
        position: relative;
        margin: 0 10px;
        transition: all 0.2s linear;
        i {
          position: absolute;
          right: 3px;
          top: 50%;
          transform: translateY(-60%) rotate(-135deg);
          width: 7px;
          height: 7px;
          border-top: 1px solid black;
          border-left: 1px solid black;
          transition: all 0.2s linear;
        }
        &::after {
          content: '';
            position: absolute;
            left: -20%;
            bottom: 0;
            width: 100%;
            height: 2px;
            // background-color: black;
            transition: all 0.2s linear;
        }
        &:hover {
          &::after {
            left: 0;
            background-color: $primary-color;
          }
          &>a {
            color: $primary-color
          }
          i {
            border-color: $primary-color;
            transform: translateY(-50%) rotate(45deg);
          }
          ol {
            display: block;
          }
        }
      }

      a {
        display: block;
        padding: 20px;
        text-transform: uppercase;
      }
    }
    ol {
      display: none;
      position: absolute;
      top: 110%;
      width: 240px;
      background-color: #31373f;
      transition: all 0.2s linear;
      a {
        color: #fff;
        padding: 10px 20px;
        font-size: 14px;
        transition: all 0.2s linear;
      }
      .sub-item {
        border-bottom: 1px solid #fff;

        &:hover {
          a {
            color: $primary-color;
          }
        }
      }
    }
  }
}
</style>