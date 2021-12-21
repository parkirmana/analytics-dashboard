<template>
    <div class="flex flex-col p-6 bg-gray-900 rounded-lg gap-y-6">
        <div class="flex justify-between items-center">
            <h2 class="text-xl font-semibold leading-loose text-white">Reviews</h2>
            <button class="flex gap-x-2 py-3 px-4 rounded-lg border border-gray-700">
                <img src="~assets/svg/chevron-down.svg" alt="">
                <span class="text-sm text-white">Today</span>
            </button>
        </div>
        <hr class="border-gray-700" />
        <div class="flex flex-col gap-y-4">
           <div v-for="order in orders.slice(0, 4)"
           :key="order.id" 
           class="flex gap-x-4 items-center">
                <img class="w-14 h-14" :src="require(`@/assets/images/${order.avatar || 'avatar1.png'}`)" alt="" />
                <div class="flex flex-col gap-y-0.5">
                <div class="text-sm font-medium text-white">{{ order.name }}</div>
                <div class="text-xs text-gray-500">{{ order.menu }}</div>
                </div>
            </div> 
        </div>
        <button
        class="py-3.5 rounded-lg w-full border border-yellow-500 text-yellow-500 text-sm font-semibold"
        >
        View all
        </button>
    </div>
</template>

<script>
import { orders } from "@/assets/data.js"
export default {
    data() {
        return {
            orders: orders
        }
    }
}
</script>

<style scoped>

</style>