<template>
    <div class="catalogItem">
        <!-- <img :src="productData.image" alt=""> -->
        <p>name {{ productData.name }}</p>
        <p>price {{ productData.price }}</p>
        <p>{{ productData.article }}</p>
        <p>{{ productData.catigory }}</p>
        <button @click="sendDataToParent">add to catr</button>
    </div>
</template>
<script>
export default {
    name: 'CatalogItem',
    props: {
        productData: {
            type: Object,
            dafault() {
                return {}
            }
        }
    },
    data(){
        return{

        }
    },
    mounted() {
        console.log(this.productData);
    },
    computed: {},
    methods: {
        sendDataToParent(){
            this.$emit('sendArticle', this.productData.article)
        }
    },
}
</script>

<style scoped >
.catalogItem {
    background: #333;
    color: #fff;
    width: 300px;
}
.catalogItem img {
    width: 50px;
    height: 50px;
}
</style>