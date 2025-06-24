<script lang="ts" setup>
const items = ref([
    { title: 'Overview', path: '/', icon: 'grommet-icons:overview' },
    { title: 'History', path: '/history', icon: 'ic:twotone-history-toggle-off' },
    // { title: 'Forecast', path: '/forecast', icon: 'material-symbols-light:calendar-today-outline' },
    // { title: 'Map', path: '/map', icon: 'material-symbols-light:map-outline' },
    { title: 'Alerts', path: '/alerts', icon: 'material-symbols-light:notifications-outline' },
    { title: 'Settings', path: '/settings', icon: 'material-symbols-light:settings-outline' },
]);

</script>
<template>
   <div>
     <header class="flex items-center gap-2 p-4 hover:scale-[101%] transition cursor-pointer">
    <p class="font-bold">AQI Monitor</p>
    </header>
    <div class="px-4 grow">
        <div class="grid gap-4">
            <NuxtLink
                v-for="item in items"
                :key="item.title"
                :to="item.path"
                class="flex items-center gap-2 p-2 rounded hover:bg-gray-200 transition-colors"
            >
                <Icon :name="item.icon" style="color: gray" />
                <span>{{ item.title }}</span>
            </NuxtLink>
        </div>
    </div>
   </div>
</template>