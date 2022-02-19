<template>
    <button
    @click="submit"
    > {{string}} </button>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
    props: {
        string: String,
        submit: Function
    }
})
</script>
