<script setup>
import { useRouter } from 'vue-router';
import { ref } from 'vue';

let routevalue = useRouter();
let headingname = 'About us';

if(routevalue.currentRoute.value.name == 'about') headingname = 'About us';
else if(routevalue.currentRoute.value.name == 'shop') headingname = 'Shop';
else headingname = 'Contact us';

let hamburger_menu = ref(false);
const hamfunc = () =>{
    hamburger_menu.value = true;
}
const closeonclick = () =>{
    hamburger_menu.value = false;
}

</script>

<template>
<section class="heading">
        <div class="header">
            <div class="left-header">
                <div class="logo">
                    <router-link to="/"><img src="../images/logo.png" /></router-link>
                </div>
                <div class="navbar">
                    <router-link to="/">Home</router-link>
                    <router-link to="/about">About us</router-link>
                    <router-link to="/shop">Shop</router-link>
                    <router-link to="/contact">Contact</router-link>
                </div>
               <router-link to="/shop"> <div class="buy">
                <button>Buy now</button>
            </div></router-link>
            </div>
            <div class="right-header">
                <div class="icons">
                    <img src="../images/shopping.gif" />
                    <img src="../images/search.svg" />
                </div>
                <div class="btn">
                    <button>My account</button>
                    <img src="../images/arrow_right.svg" />
                </div>
            </div>
            <div class="hamburger">
                <img src="../images/hamburger_menu.svg" @click="hamfunc()" />
            </div>
        </div>
        <!-- Hamburger Navbar -->
        <div class="separatenavbar animate__animated" :class="hamburger_menu? 'show' && 'animate__fadeInRight' : 'hide'">
                <div class="img">
                    <img src="../images/close.svg" id="close" @click="closeonclick()"/>
                </div>
                <router-link to="/">Home</router-link>
                <router-link to="/about">About us</router-link>
                <router-link to="/shop">Shop</router-link>
                <router-link to="/contact">Contact</router-link>
                <router-link to="/shop"><button>Buy now</button></router-link>
                <button>My account</button>
            </div>
        <div class="title">
            <h1>{{ headingname }}</h1>
        </div>
    </section>


</template>