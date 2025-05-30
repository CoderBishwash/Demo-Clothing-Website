<script setup>

const props = defineProps({
        deals: {
            type: Array,
            default: []
        }
   });

</script>

<template>
 <section class="part2">
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
                    <li v-for="deal in deals" :key="deal.id">
                        <img :src="deal.image"/>
                        <div class="star" v-if="deal.showMe" ><img src="../images/star.svg" /></div>
                        <span>{{ deal.spa }}</span>
                        <div class="costs" v-if="deal.showcost" >
                            <p>{{ deal.para }}</p><strong>&pound;11.20</strong>
                        </div>
                        <p v-if="deal.showcost == false" >{{ deal.para }}</p>
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