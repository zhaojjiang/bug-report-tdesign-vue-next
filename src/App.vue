<!-- COMMENT -->
<script setup lang="ts">
import { ref } from "vue";
import { Popup } from "tdesign-vue-next";

const show = ref(false);
</script>

<template>
  <div class="app">
    <Popup trigger="click" :destroy-on-close="true">
      <template #content>
        <div class="line-clamp-5 w-[200px] break-all">
          {{ "222".repeat(100) }}
        </div>
      </template>
      222
    </Popup>

    <div class="line-clamp-5 w-[200px] break-all" @click="show = !show">
      {{ "222".repeat(100) }}
    </div>

    <div
      v-if="show"
      style="position: absolute; top: 0px; left: 0px; width: 100%"
    >
      <div
        data-td-popup="m85rqk80"
        class="t-popup"
        data-popper-placement="top"
        style="
          position: absolute;
          inset: auto auto 0px 0px;
          margin: 0px;
          transform: translate3d(79.5px, 263.5px, 0px);
        "
      >
        <div class="t-popup__content">
          <div data-v-7a7a37b1="" class="line-clamp-5 w-[200px] break-all">
            {{ "222".repeat(100) }}
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.line-clamp-5 {
  display: -webkit-box;
  -webkit-line-clamp: 5;
  -webkit-box-orient: vertical;
  overflow: hidden;
}
.w-\[200px\] {
  width: 200px;
}

.break-all {
  word-break: break-all;
}
</style>
