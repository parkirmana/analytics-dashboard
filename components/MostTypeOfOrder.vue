<template>
    <div class="flex flex-col p-6 bg-gray-900 rounded-lg gap-y-6">
        <div class="flex justify-between items-center">
            <h4 class="text-lg font-medium leading-loose text-white">Current Occupied Spot</h4>
            <button class="flex gap-x-2.5 py-3 px-4 rounded-lg border border-gray-700">
                <img src="~assets/svg/chevron-down.svg" alt="">
                <span class="text-sm text-white">Today</span>
            </button>
        </div>
        <hr class="border-gray-700" />
        <div class="flex gap-x-7">
            <img width="176" src="~assets/images/chart.svg" alt="" />
            <div class="flex flex-col gap-y-4">
                <div class="flex gap-x-2 items-start">
                    <div class="w-4 h-4 mt-0.5 rounded-full bg-accent-red" />
                    <div>
                        <div class="text-sm font-medium text-white">Basement</div>
                        <div class="text-xs text-gray-500">200 customers</div>
                    </div>
                </div>
                <div class="flex gap-x-2 items-start">
                    <div class="w-4 h-4 mt-0.5 rounded-full bg-accent-orange" />
                    <div>
                        <div class="text-sm font-medium text-white">Fisrt Floor</div>
                        <div class="text-xs text-gray-500">122 customers</div>
                    </div>
                </div>
                <div class="flex gap-x-2 items-start">
                    <div class="w-4 h-4 mt-0.5 rounded-full bg-accent-blue" />
                    <div>
                        <div class="text-sm font-medium text-white">Second Floor</div>
                        <div class="text-xs text-gray-500">264 customers</div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>

</style>