<template>
    <div class="catalog">catalog</div>
    <CatalogItem
        v-for="product in products" :key="product.article"
        v-bind:productData="product"
        @sendArticle="ShowChildArticle"
    />
</template>

<script>
import CatalogItem from './CatalogItem.vue';
export default {
    name: 'Catalog',
    components: {
        CatalogItem,
    },
    props: {},
    data(){
        return{
            products: [
                {
                    image: "1.jpg",
                    name: "T-shirt 1",
                    price: 2100.234234234,
                    article: "T1",
                    available: true,
                    category: "Мужские"
                },
                {
                    image: "2.jpg",
                    name: "T-shirt 2",
                    price: 3150.12312412,
                    article: "T2",
                    available: true,
                    category: "Женские"
                },
                {
                    image: "3.jpg",
                    name: "T-shirt 3",
                    price: 4200.51524,
                    article: "T3",
                    available: false,
                    category: "Женские"
                },
                {
                    image: "4.jpg",
                    name: "T-shirt 4",
                    price: 5300.1245512,
                    article: "T4",
                    available: true,
                    category: "Мужские"
                },
            ]
        }
    },
    computed: {},
    methods: {
        ShowChildArticle(data) {
            console.log(data)
        }
    },
}
</script>

<style scoped></style>