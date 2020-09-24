<template>
    <div class="flex min-h-screen h-full md:max-w-screen-sm md:mx-auto lg:max-w-screen-md">
        <!-- <sidebar></sidebar> -->
        <router-view></router-view>
    </div>
</template>

<script>
// @ is an alias to /src
// import Sidebar from '@/components/Sidebar.vue'

export default {
    name: 'Home',
    components: {
        // Sidebar
    }
}
</script>
