<template>
  <div
    class="fixed bottom-0 z-20 w-full border-t border-section-div bg-layer-2"
  >
    <nav>
      <ul class="flex">
        <li v-for="(item, index) in menuItems" :key="index" class="flex-1">
          <MenuMobileSelector
            class="rounded-none"
            :label="item.label"
            :routeUrl="item.routeUrl"
            :iconUrl="item.iconUrl"
            :selected="isActive(item.routeUrl)"
            :active="true"
          />
        </li>
      </ul>
    </nav>
  </div>
</template>

<script setup lang="ts">
const isActive = (routeUrl: string) => {
  return isRouteActive(routeUrl);
};
</script>
