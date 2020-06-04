<template>
    <div class="outer-wrapper">
        <div class="line"></div>
        <div class="inner-wrapper with-padding">
            <div class="content-wrapper">
                <SharedTitleBlueUnderline 
                    :title="this.data.section_title"
                    :text="this.data.section_subtitle"
                />
                <div class="cards">
                    <el-card :body-style="{ padding: '0px' }" v-for="item in data.image_link_boxes" :key="item.id" >
                        <a :href="item.link">
                            <img :src="'http://localhost:1337' + item.image.url" class="image">
                            <div>
                                <h5 class="white">{{item.title}}</h5>
                            </div>
                        </a>
                    </el-card>
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
        //console.log("homepageintro", this.data);
    },
}
</script>

<style scoped lang="scss">
    .cards{
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        column-gap: 30px;
        margin-top: 60px;
        > div{
            border-radius: 0;
            background-color: $color-headlines;
            text-align: center;
            &:hover{
                background-color: $color-brand;
            }
        }
        a{
            text-decoration: none;
        }
        h5{
            padding: 20px 0;
        }
    }
    .outer-wrapper{
        background-color: #FFFFFF;
    }
</style>
