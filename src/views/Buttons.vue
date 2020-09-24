<template>
<div class="p-8 flex-1">
    <div class="mt-12">
        <h1 class="heading">Buttons</h1>
    </div>
    <!-- Button Variant : Base/Default -->
    <div class="row">
        <div>
            <p class="code">&lt;Button /&gt;</p>
            <Button>Default</Button>
        </div>
        <div>
            <p class="code text-gray-3">&:hover, &:focus</p>
            <Button ref="baseHover">Default</Button>
        </div>
    </div>
    <!-- Button Variant : Outline -->
    <div class="row">
        <div>
            <p class="code">&lt;Button variant="outline" /&gt;</p>
            <Button variant="outline">Default</Button>
        </div>
        <div>
            <p class="code text-gray-3">&:hover, &:focus</p>
            <Button variant="outline" ref="outlineHover">Default</Button>
        </div>
    </div>
    <!-- Button Variant : Text -->
    <div class="row">
        <div>
            <p class="code">&lt;Button variant="text" /&gt;</p>
            <Button variant="text">Default</Button>
        </div>
        <div>
            <p class="code text-gray-3">&:hover, &:focus</p>
            <Button variant="text" ref="textHover">Default</Button>
        </div>
    </div>
    <!-- Button : disableShadow -->
    <div class="row">
        <div>
            <p class="code">&lt;Button disableShadow /&gt;</p>
            <Button color="primary" disableShadow>Default</Button>
        </div>
    </div>
    <!-- Button : disabled && variant="text" disabled -->
    <div class="row">
        <div>
            <p class="code">&lt;Button disabled /&gt;</p>
            <Button disabled>Disabled</Button>
        </div>
        <div>
            <p class="code">&lt;Button variant="text" disabled /&gt;</p>
            <Button variant="text" disabled>Disabled</Button>
        </div>
    </div> 
    <!-- Button : Icon at start -->
    <div class="row">
        <div>
            <p class="code">&lt;Button startIcon="local_grocery_store" /&gt;</p>
            <Button color="primary" startIcon="local_grocery_store">
                Default
            </Button>
        </div>
        <div>
            <p class="code">&lt;Button endIcon="local_grocery_store" /&gt;</p>
            <Button color="primary" endIcon="local_grocery_store">
                Default
            </Button>
        </div> 
    </div>
    <!-- Button size : sm,md,lg -->
    <div class="row">
        <div>
            <p class="code">&lt;Button size="sm" /&gt;</p>
            <Button color="primary" size="sm">
                Default
            </Button>
        </div>
        <div>
            <p class="code">&lt;Button size="md" /&gt;</p>
            <Button color="primary" size="md">
                Default
            </Button>
        </div> 
        <div>
            <p class="code">&lt;Button size="lg" /&gt;</p>
            <Button color="primary" size="lg">
                Default
            </Button>
        </div> 
    </div>
    <!-- Button color  : default,priamry,secondary,danger  -->
    <div class="row">
        <div>
            <p class="code">&lt;Button color="default" /&gt;</p>
            <Button color="default">
                Default
            </Button>
        </div>
        <div>
            <p class="code">&lt;Button color="primary" /&gt;</p>
            <Button color="primary">
                Default
            </Button>
        </div> 
        <div>
            <p class="code">&lt;Button color="secondary" /&gt;</p>
            <Button color="secondary" >
                Secondary
            </Button>
        </div> 
        <div>
            <p class="code">&lt;Button color="danger" /&gt;</p>
            <Button color="danger" >
                Danger
            </Button>
        </div> 
    </div>
    <!-- Button color hover-focus state : default,priamry,secondary,danger  -->
    <div class="row">
        <div class="w-1/2 lg:w-auto">
            <p class="code">&:hover, &:focus</p>
            <Button color="default">
                Default
            </Button>
        </div>
        <div class="w-1/2 lg:w-auto">
            <p class="code">&:hover, &:focus</p>
            <Button color="primary">
                Default
            </Button>
        </div> 
        <div class="w-1/2 lg:w-auto">
            <p class="code">&:hover, &:focus</p>
            <Button color="secondary" >
                Secondary
            </Button>
        </div> 
        <div class="w-1/2 lg:w-auto">
            <p class="code">&:hover, &:focus</p>
            <Button color="danger" >
                Danger
            </Button>
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
}
</script>

<style lang="scss">
.row > div{
    margin: 1rem 0;
}
</style>
