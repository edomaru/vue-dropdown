<template>
    <div class="dropdown">
      <slot name="trigger" />
      <ul class="dropdown-menu show" :style="menuStyles">
        <slot name="menu" />
      </ul>
    </div>
</template>

<script>
export default {
    computed: {
        menuStyles () {
            return {
                position: 'absolute', 
                inset: '0px auto auto 0px',
                margin: '0px',
                transform: 'translate(0px, 40px)'
            }
        }
    }
}
</script>