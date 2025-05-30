<script setup>

const deliveryObjs = [
    {
        id: 1,
        line: '-How it Works'
    },
    {
        id: 2,
        line: '-Free Delivery'
    },
    {
        id: 3,
        line: '-FAQ'
    },
    {
        id: 4,
        line: '-Payment methods'
    },
    {
        id: 5,
        line: '-Delivery areas'
    },
];

const customerserviceObj = [
    {
        id: 1,
        line: '-Orders'
    },
    {
        id: 2,
        line: '-Downloads'
    },
    {
        id: 3,
        line: '-Addresses'
    },
    {
        id: 4,
        line: '-Account details'
    },
    {
        id: 5,
        line: '-Logout'
    },
    {
        id: 6,
        line: '-Lost password'
    }
];

const usefullinksObj = [
{
        id: 1,
        line: '-Contact us'
    },
    {
        id: 2,
        line: '-Help & About us'
    },
    {
        id: 3,
        line: '-Shipping & Returns'
    },
    {
        id: 4,
        line: '-Refund Policy'
    }
];

</script>
<template>
<section class="footer">
        <div class="wrapper">
            <div class="contacts">
                <div class="logo">
                    <img src="../images/logo.png" />
                </div>
                <div class="mobile">
                    <img src="../images/phone.svg" />
                    <p>+61 (0) 383 766 284</p>
                </div>
                <div class="mail">
                    <img src="../images/mail.svg" />
                    <p>noreply@envato.com</p>
                </div>
                <div class="images">
                    <img src="../images/clothing2-footer-pic1.png" />
                </div>
            </div>
            <div class="ul1">
                <ul>
                    <li>
                        <strong>Delivery</strong>
                        <ul>
                            <li v-for="line1  in deliveryObjs" :key="line1.id">
                                <router-link to="#">{{ line1.line }}</router-link>
                            </li>
                        </ul>
                    </li>
                </ul>
            </div>
            <div class="ul2">
                <ul>
                    <li>
                        <strong>Customer service</strong>
                        <ul>
                            <li v-for="line2 in customerserviceObj" :key="line2.id">
                                <router-link to="#">{{ line2.line }}</router-link>
                            </li>
                        </ul>
                    </li>
                </ul>
            </div>
            <div class="ul3">
                <ul>
                    <li>
                        <strong>Useful links</strong>
                        <ul>
                            <li v-for="line3 in usefullinksObj" >
                                <router-link to="#">{{ line3.line }}</router-link>
                            </li>
                        </ul>
                    </li>
                </ul>
            </div>
        </div>
        <div class="line">

        </div>
        <div class="bottom-wrapper">
            <div class="copywright">
                <p>&copy; 2021 - BeTheme. Muffin group - HTML by BeantownThemes</p>
            </div>
            <div class="policies">
                <router-link to="#">Terms and conditions</router-link>
                <router-link to="#">Privacy policy</router-link>
                <router-link to="#">Cookies</router-link>
                <router-link to="#"><img src="../images/arrowup.svg" /></router-link>
            </div>
        </div>
    </section>



</template>