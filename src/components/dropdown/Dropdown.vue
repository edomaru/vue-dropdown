<template>
    <div class="dropdown" v-click-out-side="handleClickOutside">
      <slot name="trigger" :toggleClass="toggleClass" :toggle="toggle" />
      <ul class="dropdown-menu" :class="toggleClass" :style="menuStyles">
        <slot name="menu" :toggle="toggle" />
      </ul>
    </div>
</template>

<script>
import clickOutSide from '@mahdikhashan/vue3-click-outside'

export default {
    directives: {
        clickOutSide
    },
    computed: {
        menuStyles () {
            return {
                position: 'absolute', 
                inset: '0px auto auto 0px',
                margin: '0px',
                transform: 'translate(0px, 40px)'
            }
        },
        toggleClass () {
            return this.isOpen ? 'show' : ''
        }
    },
    data: () => ({
        isOpen: false
    }),
    methods: {
        toggle () {
            this.isOpen = !this.isOpen
        },
        handleClickOutside () {
            this.isOpen = false
        }
    }
}
</script>