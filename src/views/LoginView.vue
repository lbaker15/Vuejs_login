<template>
    <div class="form">
        <span>
        <label>Username</label>
        <Input @inputVal="input" />
        </span>
        <Button string="Submit" :submit="submit" />
    </div>
</template>

<script>
    import Button from '@/components/Button.vue'
    import Input from '@/components/Input.vue'
    import '@/assets/css/style.scss'
    import router from '@/router'
    export default {
        components: { Button, Input },
        data() {
            return {
                inputVal: ''
            }
        },
        methods: {
            submit(e) {
                console.log(e, this.inputVal)
                //Set token
                if (this.inputVal.length > 3) {
                router.push('/')
                }
            },
            input(value) {
                this.inputVal = value
            }
        }
    }
</script>