<template>
<div class="flex min-h-screen h-full">
    <sidebar></sidebar>
    <router-view></router-view>
    <!-- <h1 class="heading">Welcome ! Explore the design pattern</h1> -->
</div>
</template>

<script>
// @ is an alias to /src
import Sidebar from '@/components/Sidebar.vue'

export default {
    name: 'Home',
    components: {
        Sidebar
    }
}
</script>
