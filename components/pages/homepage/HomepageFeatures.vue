<template>
    <div class="outer-wrapper">
        <div class="inner-wrapper with-padding">
            <div class="content-wrapper">
                <div class="features">
                    <div class="feature" v-for="item in data.feature" :key="item.id">
                        <img :src="'http://localhost:1337' + item.icon.url" :alt="item.icon.alternativeText">
                        <h4>{{item.text}}</h4>
                    </div>
                </div>
            </div><!-- .content-wrapper -->
        </div><!-- .inner-wrapper -->
        <div class="line"></div>
    </div><!-- .outer-wrapper -->
</template>

<script>
export default {
    props:{
        data: Object,
    },
    mounted(){
        //console.log("homepageFeatures", this.data);
    },
}
</script>

<style scoped lang="scss">
    .outer-wrapper{
        background-color: $bg-neutral;
    }
    .features{
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        column-gap: 30px;
        text-align: center;
        h4{
            margin-top: 45px;
        }
    }
</style>
