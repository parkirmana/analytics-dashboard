<template>
    <div class="flex gap-6">
        <StatsCard 
            v-for="stat in stats"
            :key="stat.id"
            :stat=stat
        />
    </div>
</template>

<script>
import { statistics } from "@/assets/data.js"
export default {
    data() {
        return {
            stats: statistics
        }
    }
}
</script>

<style scoped>

</style>