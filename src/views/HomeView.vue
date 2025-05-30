<script setup>
import Services from '@/HomeComponent/Services.vue';
import Header from '../HomeComponent/Header.vue';
import WeeklyDeals1 from '../HomeComponent/WeeklyDeals1.vue';
// import WeeklyDeals2 from '../HomeComponent/WeeklyDeals2.vue';
import WhoWeAre from '../HomeComponent/WhoWeAre.vue';
import OffSale from '@/HomeComponent/OffSale.vue';
import Footer from '@/HomeComponent/Footer.vue';

const clothObjs = [ 
    {
        id: 1,
        image: '../src/images/clothing2-products-pic8-300x300.jpg',
        spa: 'Quisque lorem tortor',
        para: '£28.00 - £30.00',
        showMe: true,
        showcost: false,
    },
    {
        id: 2,
        image: '../src/images/clothing2-products-pic7-300x300.jpg',
        spa: 'Curabitur et ligula',
        para: '£12.50',
        showMe: true,
        showcost: true,
    },
    {
        id: 3,
        image: '../src/images/clothing2-products-pic6-300x300.jpg',
        spa: 'Etiam ullamcorper',
        para: '£12.00',
        showMe: false,
        showcost: false,
    },
    {
        id: 4,
        image: '../src/images/clothing2-products-pic5-300x300.jpg',
        spa: 'Nulla imperdiet sit amet',
        para: '£25.00',
        showMe: false,
        showcost: false,
    },
];
const clothObjs2 = [ 
    {
        id: 1,
        spa: 'Aliquam erat ac ipsum',
        para: '£24.00',
        showMe: false,
        showcost: false,
        image: '../src/images/clothing2-products-pic2-300x300.jpg'
    },
    {
        id: 2,
        spa: 'Aliquam sem',
        para: '£16.00',
        showMe: false,
        showcost: false,
        image: '../src/images/clothing2-products-pic11-300x300.jpg'
    },
    {
        id: 3,
        spa: 'Curabitur et ligula',
        para: '£12.50',
        showMe: true,
        showcost: true,
        image: '../src/images/clothing2-products-pic7-300x300.jpg'
    },
    {
        id: 4,
        spa: 'Etiam ullamcorper',
        para: '£12.00',
        showMe: false,
        showcost: false,
        image: '../src/images/clothing2-products-pic6-300x300.jpg'
    },
];

document.title = 'Home';
 
</script>

<template>

<Header />

<WeeklyDeals1 class="part2"  :deals="clothObjs" />

<WeeklyDeals1 class="part3" :deals="clothObjs2" />

<!-- <WeeklyDeals2 /> -->

<WhoWeAre />

<Services />

<OffSale />

<Footer />

</template>