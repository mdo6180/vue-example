<template>
    <div id="App" class="flex container h-screen w-full">
        <div class="w-1/5 border-r border-lighter px-8 py-2">
            <button class="h-12 w-12 hover:bg-blue-100 text-3xl text-blue-400 rounded-full border-black">
                <i class="fa fa-twitter"></i>
            </button>
            <div>
                <button v-for="tab in tabs" :key="tab.id" class="flex items-center py-2 px-4 hover:bg-blue-100 rounded-full mr-auto mb-3 text-blue-400">
                    <i :class="`${tab.icon} text-2xl mr-4 text-left`"></i>
                    <p class="text-lg font-semibold text-left">{{ tab.title }}</p>
                </button>
            </div>
        </div>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
    name: 'App',
    components: {},
    data() {
        return {
            tabs: [
                {icon: 'fa fa-home', title: 'Home', id: 'home'},
                {icon: 'fa fa-hashtag', title: 'Explore', id: 'explore'}
            ]
        }
    }
});
</script>

<style>
</style>
