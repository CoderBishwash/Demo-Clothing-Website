<script setup>
import { ref } from 'vue';

let hamburger_menu = ref(false);
const hamfunc = () =>{
    hamburger_menu.value = true;
}
const closeonclick = () =>{
    hamburger_menu.value = false;
}

</script>
<template>

    <section class="part1">
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
                    <div class="buy">
                        <router-link to="/shop"><button>Buy now</button></router-link>
                    </div>
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
                    <img src="../images/hamburger_menu.svg" id="hambtn" @click="hamfunc()"/>
                </div>
            </div>
            <div class="container">
                <div class="spring">
                    <div class="top">
                        <span>2020</span>
                        <div class="line"></div>
                    </div>
                    <div class="mid">
                        <div class="imgs">
                            <img src="../images/arrowleft.svg" />
                            <img src="../images/arrowright.svg" />
                        </div>
                        <div class="words">
                            <p>Spring <br> collection</p>
                        </div>
                    </div>
                    <div class="bottom">
                        <p>spring sale | up to 50% off</p>
                        <router-link to="/shop"><button>Our collection</button></router-link>
                    </div>
                </div>
                <div class="images">
                    <div class="top-image">
                        <img src="../images/clothing2-slider-pic4.png" />
                    </div>
                    <div class="bottom-images">
                        <div class="img1"> 
                        <img src="../images/clothing2-slider-pic2.jpg" />
                        <p>Woman</p>
                        <div class="line"></div>
                    </div> 
                        <div class="img2"> 
                        <img src="../images/clothing2-slider-pic3.jpg" />
                        <p>Men</p>
                        <div class="line"></div>
                    </div>
                    </div>
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
    </section> 

</template>