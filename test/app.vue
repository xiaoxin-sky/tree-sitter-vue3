<template>
  <div :class="[env.isDarkTheme ? 'night' : 'day']">
    <Suspense>
      <template #default>
        <router-view />
      </template>
      <template #fallback>
        <div>加载中...</div>
      </template>
    </Suspense>
  </div>
</template>

<script lang="ts">
import { env } from "gkoudai-private-front-lib";
import { defineComponent } from "vue";

export default defineComponent({
  components: {},
  setup() {
    return { env };
  },
});
</script>

<style lang="scss"></style>
