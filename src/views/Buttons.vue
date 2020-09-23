<template>
<div class="px-24 flex-1">
    <div class="mt-12">
        <h1 class="heading">Buttons</h1>
    </div>
    <div class="row md:w-1/2">
        <div>
            <p class="code">&lt;Button /&gt;</p>
            <Button></Button>
        </div>
        <div>
            <p class="code">&:hover, &:focus</p>
            <Button ref="defaultHover"></Button>
        </div>
    </div>
</div>
</template>

<script>
import Button from '@/components/Buttons.vue'

export default {
    name: 'ButtonView',
    components: {
        Button,
    },
    mounted(){
        this.$refs.defaultHover.$el.focus();
    },
}
</script>

<style>

</style>
