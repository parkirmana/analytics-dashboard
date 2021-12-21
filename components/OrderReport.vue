<template>
    <div class="p-6 bg-gray-900 rounded-lg">
        <div class="flex justify-between items-center pb-4">
            <h2 class="text-xl font-semibold leading-loose text-white">Transactions Report</h2>
            <button class="flex py-3 px-4 rounded-lg border border-gray-700 gap-x-2.5">
              <img src="~assets/svg/options.svg" alt="">
              <span class="text-sm text-white">Filter order</span>
            </button>
        </div>
        <table class="w-full">
            <thead>
                <tr class="text-sm font-semibold text-white">
                <td class="py-4 border-b border-gray-700">Customer</td>
                <td class="py-4 border-b border-gray-700">Slot</td>
                <td class="py-4 border-b border-gray-700">Time</td>
                <td class="py-4 border-b border-gray-700 text-right">Total Payment</td>
                <td class="py-4 border-b border-gray-700 text-center">Status</td>
                </tr>
            </thead>
            <tbody>
                <tr v-for="order in orders" 
                :key="order.id"
                :order=order
                class="text-sm text-gray-500">
                    <td class="py-4">
                        <div class="flex gap-4 items-center">
                        <img width="32" :src="require(`@/assets/images/${order.avatar || 'avatar1.png'}`)" alt="" />
                        <span> {{ order.name }} </span>
                        </div>
                    </td>
                    <td class="py-4">{{ order.slot }}</td>
                    <td class="py-4">{{ order.time }}</td>
                    <td class="py-4 tabular-nums text-right">{{ order.total }}</td>
                    <td class="py-4 flex justify-center">
                        <span
                        class="flex justify-center py-1 w-24 font-medium capitalize rounded-full bg-opacity-20"
                        :class="{
                            'bg-green-200 text-green-400': order.status === 'completed',
                            'bg-purple-200 text-purple-400': order.status === 'parking',
                            'bg-yellow-200 text-yellow-400': order.status === 'pending',
                        }"
                        >
                        {{ order.status }}
                        </span>
                    </td>
                </tr>
            </tbody>
        </table>
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