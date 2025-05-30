<script setup>

const shopObj = [
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
    {
        id: 5,
        spa: 'Lorem ipsum dolor sit amet',
        para: '£12.50',
        showMe: false,
        showcost: true,
        image: '../src/images/clothing2-products-pic2-300x300.jpg'
    },
    {
        id: 6,
        spa: 'Nulla imperdiet sit amet',
        para: '£25.00',
        showMe: false,
        showcost: false,
        image: '../src/images/clothing2-products-pic5-300x300.jpg'
    },
    {
        id: 7,
        spa: 'Nullam wisi ultricies',
        para: '£12.50',
        showMe: false,
        showcost: false,
        image: '../src/images/clothing2-products-pic10-300x300.jpg'
    },
    {
        id: 8,
        spa: 'Quisque cursus et porttitor risus',
        para: '£17.00',
        showMe: false,
        showcost: false,
        image: '../src/images/clothing2-products-pic9-300x300.jpg'
    },
    {
        id: 9,
        spa: 'Quisque lorem tortor',
        para: '£29.00',
        showMe: true,
        showcost: true,
        image: '../src/images/clothing2-products-pic4-300x300.jpg'
    },
    {
        id: 10,
        spa: 'Quisque lorem tortor',
        para: '£28.00 - £30.00',
        showMe: true,
        showcost: false,
        image: '../src/images/clothing2-products-pic8-300x300.jpg'
    },
    {
        id: 11,
        spa: 'Quisque lorem tortor',
        para: '£70.00 - £85.00',
        showMe: true,
        showcost: false,
        image: '../src/images/clothing2-products-pic12-300x300.jpg'
    },
    {
        id: 12,
        spa: 'Vestibulum dapibus',
        para: '£32',
        showMe: false,
        showcost: false,
        image: '../src/images/clothing2-products-pic3-300x300.jpg'
    }
];
</script>

<template>
<section class="shop-part1">
        <div class="wrapper">
            <b>Showing all 12 results</b>
            <div class="top-lists">
                <ul>
                    <li v-for="lists in shopObj" :key="lists.id">
                        <img :src="lists.image" />
                        <div class="star" v-if="lists.showMe"><img src="./../images/star.svg" /></div>
                        <span>{{ lists.spa }}</span>
                        <div class="costs" v-if="lists.showcost">
                            <p>{{ lists.para }}</p><strong>&pound;11.20</strong>
                        </div>
                        <p v-if="lists.showcost == false">{{ lists.para }}</p>
                    </li>
                </ul>
            </div>
        </div>
    </section>


</template>