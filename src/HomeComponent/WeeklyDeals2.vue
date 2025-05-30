<script setup>

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

</script>
<template>
<section class="part3">
        <div class="wrapper">
            <div class="top">
                <div class="left">
                    <span>Featured</span>
                    <h1>Weekly deals</h1>
                </div>
                <div class="right">
                    <div class="line"></div>
                </div>
            </div>
            <div class="bottom">
                <ul>
                    <li v-for="deals in clothObjs2" :key="deals.id">
                        <img :src="deals.image"/>
                        <div class="star" v-if="deals.showMe" ><img src="../images/star.svg" /></div>
                        <span>{{ deals.spa }}</span>
                        <div class="costs" v-if="deals.showcost" >
                            <p>{{ deals.para }}</p><strong>&pound;11.20</strong>
                        </div>
                        <p v-if="deals.showcost == false" >{{ deals.para }}</p>
                    </li>
                </ul>
                <router-link to="/shop"><div class="btn">
                    <button>See all products</button>
                    <img src="../images/arrow_right.svg" />
                </div></router-link>
            </div>
        </div>
    </section>



</template>