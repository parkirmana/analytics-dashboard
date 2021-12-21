<template>
    <div class="flex flex-col p-4 w-1/3 bg-gray-900 rounded-lg gap-y-3">
        <div class="flex items-center gap-x-3">
            <div class="p-2 bg-gray-800 rounded-lg">
                <img :src="require(`@/assets/svg/${stat.icon || 'store.svg'}`)" alt="">
            </div>
            <span
                class="text-xs font-medium"
                :class="stat.status === 'up' ? 'text-green-400' : 'text-red-500'"
            >
            {{ stat.percentage }}
            </span>
            <div
                class="p-0.5 rounded-full bg-opacity-20"
                :class="stat.status === 'up' ? 'bg-green-200' : 'bg-red-200'"
            >
                <div v-if="stat.status === 'up'" class="fill-current text-green-400">
                    <img src="~assets/svg/arrowUp.svg" alt="">
                </div>
                <div v-else class="fill-current text-red-500">
                    <img src="~assets/svg/arrowDown.svg" alt="">
                </div>
            </div>
        </div>
        <div class="text-3xl font-semibold text-white">{{ stat.value }}</div>
        <div class="text-sm tracking-wide text-gray-500">{{ stat.title }}</div>
    </div>
</template>

<script>
export default {
    props: ['stat']
}
</script>

<style scoped>

</style>