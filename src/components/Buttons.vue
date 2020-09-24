<template>
<button :class="[variantType,colorType,buttonSize]" class="flex items-center">
    <template v-if="isStartIcon"><i class="material-icons mr-2">{{ startIcon }}</i></template>
    <slot></slot>
    <template v-if="isEndIcon"><i class="material-icons ml-2">{{ endIcon }}</i></template>
</button>
</template>

<script>
export default {
    name: 'button',
    props: {
        variant: {
            type: String,
            default: "base",
        },
        disabled: Boolean,
        startIcon: String,
        endIcon: String,
        size: String,
        color: String
    },
    computed: {
        //Returns style based on the type of variant
        variantType() {
            if (this.disabled) {
                return `disabled-${this.variant}`;
            } else {
                return `btn-${this.variant}`;
            }
        },
        //Returns button color based on the type of color
        colorType() {
            if (this.color) {
                return `btn-${this.color}`;
            } else {
                return "";
            }
        },
        //Returns the class based on the size of the button
        buttonSize() {
            if (this.size) {
                return `btn-${this.size}`;
            } else {
                return '';
            }
        },
        //Return true if button contains an start icon
        isStartIcon() {
            return this.startIcon ? true : false;
        },
        //Return true if button contains an end icon
        isEndIcon() {
            return this.endIcon ? true : false;
        }
    },
}
</script>

<style lang="scss" scoped>
@import url("https://fonts.googleapis.com/icon?family=Material+Icons");

// Button : Base
.btn-base {
    @apply bg-gray-5 shadow-1 rounded-6px py-2 px-4 font-noto font-medium text-sm text-center leading-5 text-gray-6
}

.btn-base:hover,
.btn-base:focus {
    @apply bg-gray-7
}

// Button : Outline
.btn-outline {
    @apply .btn-base border border-blue-1 text-blue-1 bg-white shadow-none
}

.btn-outline:hover,
.btn-outline:focus {
    background: rgba(41, 98, 255, 0.1);
}

// Button :  Text
.btn-text {
    @apply .btn-base text-blue-1 bg-transparent shadow-none
}

.btn-text:hover,.btn-text:focus {
    background: rgba(41, 98, 255, 0.1);
}

//  Shadow : Disabled
Button[disableShadow] {
    @apply shadow-none
}

// Button : Color : Base/Default
.btn-primary {
    @apply bg-primary text-white shadow-2
}

.btn-primary:hover,
.btn-primary:focus {
    @apply bg-primary-hover
}

// Button : Color : Secondary
.btn-secondary {
    @apply bg-secondary text-white shadow-3
}

.btn-secondary:hover,
.btn-secondary:focus {
    @apply bg-secondary-hover
}

// Button : Color : Danger
.btn-danger {
    @apply bg-danger text-white shadow-2
}

.btn-danger:hover,
.btn-danger:focus {
    @apply bg-danger-hover
}

//Button : Disabled : Base/Default
.disabled-base {
    @apply .btn-base cursor-not-allowed text-gray-1
}

//Button : Disabled : Text variant
.disabled-text {
    @apply .btn-text cursor-not-allowed text-gray-1
}
//Button : Size : sm
.btn-sm{ 
    @apply py-6px px-3
}
//Button : Size : md
.btn-md{ 
    @apply py-2 px-4 
}
//Button : Size : lg
.btn-lg{ 
    @apply py-11px px-22px
}
</style>
