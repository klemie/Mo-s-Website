<template>
    <div class="nav d-flex p-2">
        <div class="mr-auto">
            <g-link to="/">
                <img height="50px" :src="logo" />
            </g-link>
        </div>
        <div class="p-2 mt-2">
            <g-link class="btn-text" to="/">HOME</g-link>
        </div>
        <div class="p-2 mt-2">
            <g-link class="btn-text" to="/about/">ABOUT</g-link>
        </div>
        <div class="p-2 mt-2">
            <g-link class="btn-text" to="/services/">SERVICES</g-link>
        </div>
        <div class="p-2 mt-2">
            <g-link class="btn-text" to="/readings/">READINGS</g-link>
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
    .nav {
        width: 100%;
    }

    .btn {
        background-color: #3D3D3D;
        border-radius: 15px!important;
        color: white;
    }

    .btn.radius {
        border-radius: 60px;
    }

    btn:hover {
        color: #E3D0C2;
    }

    .btn-text {
        background-image: 
            linear-gradient(
                transparent 0%,
                transparent 90%,
                #E3D0C2 90%,
                #E3D0C2 100%
            );
        background-repeat: no-repeat;
        background-size: 0% 100%;
        background-position-x: right;
        transition: background-size 400ms;
    }

    .btn-text:hover {
        background-size: 100% 100%;
        background-position-x: left;
        color: #E3D0C2;
    }
    .btn-text.active {
        color: #E3D0C2;
    }
</style>