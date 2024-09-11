<template>
  <NuxtLink to="/">
    <slot />
  </NuxtLink>
</template>

<style lang="scss" scoped>
a {
  display: block;
  padding: 17px 30px;
  background-color: #e8734a;
  text-transform: capitalize;
  color: #fff;
  font-weight: 500;
  &:hover {
    background-color: #00997d;
  }
}
</style>