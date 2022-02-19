<template>
    <input 
    v-bind:class="[{activeInput: valid}, 'input']"
    v-on:input="updateValue($event.target.value)"
     />
</template>

<script>
    export default {
        data() {
            return {
                valid: false
            }
        },
        methods: {
            updateValue: function (value) {
                if (value.length > 3) {
                    this.valid = true

                }
                this.$emit('inputVal', value);
            }
        }
    }
</script>

<style scoped lang="scss">
    .input {
        border: 1px solid red;
        outline: none;
    }
    .activeInput {
        border: 1px solid green;
    }
</style>