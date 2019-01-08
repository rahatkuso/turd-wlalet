<template>
<span>
    {{ value }} Turd
</span>
</template>

<script>
export default {
    name: "FormatTurd",
    props: {
        amount: {
            type: Number,
            required: true
        },
        round: {
            type: Boolean,
            required: false,
            default: false
        }
    },
    computed: {
        value () {
            let value = this.amount / 1e9
            if(this.round)
                value = value.toFixed(3)
            return value.toLocaleString()
        }

    }
}
</script>

<style>
</style>
