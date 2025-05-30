<script setup>

let ServiceObjs = [
    {
        id: 1,
        spa: 'Always free shipping',
        image: '../src/images/clothing2-home-icon1.png',
        para: 'Lorem ipsum dolor sit amet mauris dolor bibendum sapien',
    },
    {
        id: 2,
        spa: '14 day return policy',
        image: '../src/images/clothing2-home-icon2.png',
        para: 'Nullam wisi ultricies gravida vitae dapibus risus',
    },
    {
        id: 3,
        spa: 'Quick delivery in 48h',
        image: '../src/images/clothing2-home-icon3.png',
        para: 'Nullam wisi ultricies gravida vitae dapibus risus',
    },
    {
        id: 4,
        spa: 'Online payment',
        image: '../src/images/clothing2-home-icon4.png',
        para: 'Lorem ipsum dolor sit amet mauris dolor bibendum sapien',
    },
];
</script>

<template>
<section class="part5">
        <ul>
            <li v-for="services in ServiceObjs">
                <img :src="services.image" />
                <span>{{ services.spa }}</span>
                <p>{{ services.para }}</p>
            </li>
        </ul>
    </section>



</template>