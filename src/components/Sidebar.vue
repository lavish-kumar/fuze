<template>
  <div>
    <a href="#" class="trigger-sidebar"><Menu /></a>
    <aside class="fadeInLeft">
      <router-link to="/">
        <Logo class="logo" />
      </router-link>
      <BaseSettings/>
      <AdvancedSettings/>
    </aside>
  </div>
</template>

<script>
import Logo from '@/assets/logo.svg';
import BaseSettings from '@/components/BaseSettings';
import AdvancedSettings from '@/components/AdvancedSettings';

export default {
  name: 'Sidebar',
  components: {
    Logo,
    BaseSettings,
    AdvancedSettings,
  },
};
</script>

<style lang="scss" scoped>
aside {
  position: absolute;
  left: 0;
  top: 0;
  width: 300px;
  background-color: var(--black-80);
  height: 100%;
  z-index: 1;
  overflow: hidden;
}

div {
  height: calc(100% - 190px);
  min-height: 400px;
}

.logo {
  display: block;
  margin: 60px auto;
  width: 70px;
}

@media all and (max-width: 768px) {
  aside {
    display: none;
  }
}
</style>
