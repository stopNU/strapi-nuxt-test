<template>
    <div>
        <div class="outer-wrapper">
            <div class="inner-wrapper">
                <div class="content-wrapper white content">
                    <div class="logos">
                        <img class="" 
                            srcset="
                                ~/assets/images/tag_logo_footer@2x.png 2x,
                                ~/assets/images/tag_logo_footer.png 1x"
                            src="~/assets/images/tag_logo_footer.png">
                        <div class="vertical-line"></div>
                        <img class="" 
                            srcset="
                                ~/assets/images/sg_logo_footer@2x.png 2x,
                                ~/assets/images/sg_logo_footer.png 1x"
                            src="~/assets/images/sg_logo_footer.png">
                            <div class="box">
                                <h6 class="white">Authorized Master Distributor of Secure Group</h6>
                            </div>
                    </div>
                    <div class="menu">
                        <ul>
                            <li><a href="#">About</a></li>
                            <li><a href="#">Menu2</a></li>
                            <li><a href="#">Menu3</a></li>
                            <li><a href="#">Menu4</a></li>
                            <li><a href="#">Menu5</a></li>
                            <li><a href="#">Menu6</a></li>
                            <li><a href="#">Menu7</a></li>
                            <li><a href="#">Menu8</a></li>
                        </ul>
                    </div>
                    <div class="address">
                        <div class="vertical-line"></div>
                        <div>
                            <span>ADDRESS</span><br> 
                            183-925 Maisonneuve Ouest,<br>
                            Montreal H3A 0A5,<br> 
                            Canada
                        </div>
                    </div>
                </div>
                <div class="copyright">

                </div>
            </div>
        </div>
     
        <div class="outer-wrapper blue-top-border">
            <div class="inner-wrapper">
                <div class="content-wrapper copyright">
                    <p class="white">© T.A.G. Consultation 2012-{{ new Date().getFullYear() }}. All Rights Reserved.</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style scoped lang="scss">
    .copyright{
        padding: 15px 0 25px;
        p{
            font-size: 12px;
        }
    }
    .logos{
        display: flex;
        align-items: center;
        > img{
            align-self: center;
        }
        .vertical-line{
            margin: 0 15px;
            height: 30px;
        }
        .box{
            background-color: $color-brand-hover;
            padding: 6px 50px 6px 10px;
            margin-left: 15px;
            h6{
                max-width: 130px;
            }
        }
    }
    .outer-wrapper{
        background-color: #010B1B;
        &.blue-top-border{
            border-top: 1px solid $color-brand-hover;
        }
    }
    .content-wrapper.content{
        padding: 50px 0 95px;
        display: grid;
        grid-template-columns: 2fr 2fr 1fr;
        align-items: center;
        .address{
            display: flex;
            align-items: center;
            font-size: 12px;
            line-height: 19px;
            span{
                font-size: 14px;
            }
        }
    }
    .vertical-line{
        border-left: 1px solid $color-brand;
        margin-right: 15px;
        height: 65px;
    }
    ul{
        list-style-type: none;
        -webkit-columns: 2;
        -moz-columns: 2;
        columns: 2;
        list-style-position: inside;//this is important addition
        li{
            a{
                font-size: 14px;
                font-weight: 400;
                line-height: 25px;
                font-family: $font-headlines;
                color: $color-white;
                text-decoration: none;
                text-transform: uppercase;
                &:hover{
                    color: $color-brand;
                }
            }
        }
    }
</style>
