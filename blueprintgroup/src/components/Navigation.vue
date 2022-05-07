<template>
    <div class="d-flex p-2">
        <div class="mr-auto">
            <g-link to="/">
                <img :src="logo" />
            </g-link>
        </div>
        <div class="p-2">
            <g-link to="/">HOME</g-link>
        </div>
        <div class="p-2">
            <g-link to="/about/">ABOUT</g-link>
        </div>
        <div class="p-2">
            <g-link to="/services/">SERVICES</g-link>
        </div>
        <div class="p-2">
            <g-link to="/readings/">READINGS</g-link>
        </div>
        <div class="p-2">
            <g-link to="/">
                <button type="button" class="btn rounded">GET IN TOUCH</button>
            </g-link>
        </div>
    </div>
</template>

<script>
import { BButton } from 'bootstrap-vue';
export default {
    components: {
        BButton
    },
    data() {
        return {
            logo: require('~/Logo.svg')
        }
    }
}
</script>

<style scoped>
    .btn {
        background-color: #3D3D3D;
        border-radius: 24px!important;
    }
    .btn.radius {
        border-radius: 60px;
    }
</style>