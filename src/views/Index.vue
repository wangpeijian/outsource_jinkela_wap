<style scoped lang="scss">
    .bg{
        background-position: center;
        background-repeat: no-repeat;
        background-size: cover;
    }

    .home {

        .header {
            color: #fff;
            height: 0.44rem;
            background: rgba(0, 0, 0, 0);
            transition: .5s;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 99;

            &.fixed-mark {
                background: #4b91ff;
            }

            .menu-btn {
                display: inline-block;
                height: .16rem;
                width: .16rem;
                background: url("../../static/svg/menu.svg") center no-repeat;
                background-size: contain;
                position: absolute;
                top: .14rem;
                left: .14rem;
            }
        }

        .banner {
            height: 7.12rem;
            color: #FFFFFF;
            background: blue;
            position: relative;

            .name {
                text-align: center;
                padding-top: .66rem;
                line-height: .36rem;

                .title {
                    font-size: .35rem;
                    padding-bottom: .1rem;
                }

                .sub-title {
                    font-size: .2rem;
                }
            }

            .phone {
                position: absolute;
                top: 1.78rem;
                left: .61rem;
                height: 4.98rem;
                width: 2.53rem;
                display: block;
            }
        }

        .data {
            height: 7.76rem;
        }

        .evaluate {
            height: 9.09rem;
            background: #F8F9FA;

            .problem {
                height: 1.83rem;
                border-bottom: 1px solid #E7E8EA;
            }

            .dialog-group {
                position: relative;
                overflow: hidden;
                height: 7.26rem;

                .dialog {
                    background: #fff;
                    border-radius: .06rem;
                    box-shadow: 0 6px 12px 0 rgba(32, 33, 39, 0.08);
                    position: absolute;
                    transition: 2.5s;
                    transform: translateX(250%);
                    width: 3.39rem;
                    left: .17rem;

                    &.fixed-mark {
                        transform: translateX(0%);
                    }

                    &.d-1 {
                        height: 1.22rem;
                        top: .3rem;
                    }

                    &.d-2 {
                        height: 1.44rem;
                        top: 1.74rem;
                    }

                    &.d-3 {
                        height: 1.27rem;
                        top: 3.37rem;
                    }

                    &.d-4 {
                        height: 1.7rem;
                        top: 4.83rem;
                    }
                }
            }
        }

        .recommend {
            height: 10.01rem;
            position: relative;
            overflow: hidden;

            .circle {
                display: inline-block;
                position: absolute;
                border-radius: 50%;

                &.circle-1 {
                    top: 0.358rem;
                    left: -1.792rem;
                    width: 5.004rem;
                    height: 5.004rem;
                    z-index: 1;
                }

                &.circle-2 {
                    top: 1.284rem;
                    left: 1.284rem;
                    width: 3.672rem;
                    height: 3.672rem;
                    z-index: 1;
                }

                &.circle-3 {
                    top: 2.5775rem;
                    left: -0.7425rem;
                    width: 5.235rem;
                    height: 5.235rem;
                    z-index: 3;
                }

                &.circle-4 {
                    top: 5.05rem;
                    left: 0.9rem;
                    width: 4.41rem;
                    height: 4.41rem;
                    z-index: 1;
                }

                &.circle-5 {
                    top: 5.34rem;
                    left: -2.07rem;
                    width: 5.56rem;
                    height: 5.56rem;
                    z-index: 2;
                }
            }
        }

        .institution {
            height: 10.02rem;

            .title {
                width: 2.98rem;
                height: .8rem;
                margin: 0 auto;
                background-size: contain;
            }

            .panel{
                width: 3.22rem;
                margin: 0 auto;
                display: block;
            }
        }

        .capital {
            height: 7.74rem;
            background: #333743;
        }

        .partner {
            height: 9.04rem;
            background: #333743;
            position: relative;

            &::after{
                content: '';
                position: absolute;
                width: .02rem;
                background: #FFFFFF;
                top: 0;
                bottom: .37rem;
                left: 50%;
                transform: translateX(-50%);
            }

            .logo-list{
                margin: 0 .3rem;
                position: relative;
                padding-top: .15rem;
                overflow: hidden;

                .item{
                    width: 50%;
                    padding: 5%;
                    float: left;
                    height: 1rem;

                    img{
                        display: block;
                        width: 100%;
                    }
                }
            }
        }

        .footer {
            height: 4.88rem;
            color: #fff;
            padding-top: .57rem;

            .qrcode{
                display: block;
                width: 1.2rem;
                margin: 0 auto;
            }

            .label{
                display: block;
                text-align: center;
                font-size: .16rem;
                line-height: .5rem;
            }

            .record{
                font-size: .14rem;
                margin: .3rem .2rem 0 .2rem;
            }
        }
    }
</style>

<template>
    <div class="home" id="homeTop">
        <header class="header" v-float-top:homeTop>
            <span class="menu-btn"></span>
        </header>

        <div class="banner">
            <div class="name">
                <h1 class="title">金客拉</h1>
                <p class="sub-title">做金融，更简单</p>
            </div>

            <div class="phone bg" :style="{'background-image': `url(${Phone})`}"></div>
        </div>

        <div class="data"></div>

        <div class="evaluate">
            <div class="problem bg" :style="{'background-image': `url(${problem})`}"></div>

            <div class="dialog-group" id="dialogGroup">
                <div class="dialog d-1" v-float-top:dialogGroup="-600"></div>
                <div class="dialog d-2" v-float-top:dialogGroup="-400"></div>
                <div class="dialog d-3" v-float-top:dialogGroup="-200"></div>
                <div class="dialog d-4" v-float-top:dialogGroup="-100"></div>
            </div>
        </div>

        <div class="recommend bg" :style="{'background-image': `url(${recommendBg})`}">
            <div class="circle circle-1 bg" :style="{'background-image': `url(${Oval1})`}"></div>
            <div class="circle circle-2 bg" :style="{'background-image': `url(${Oval2})`}"></div>
            <div class="circle circle-3 bg" :style="{'background-image': `url(${Oval3})`}"></div>
            <div class="circle circle-4 bg" :style="{'background-image': `url(${Oval4})`}"></div>
            <div class="circle circle-5 bg" :style="{'background-image': `url(${Oval5})`}"></div>
        </div>

        <div class="institution">
            <div class="title bg" :style="{'background-image': `url(${companyBg})`}"></div>

            <img class="panel" :src="copy1">
            <img class="panel" :src="copy1">
            <img class="panel" :src="copy1">
            <img class="panel" :src="copy1">
        </div>

        <div class="capital">

        </div>

        <div class="partner">
            <ul class="logo-list">
                <li class="item"><img :src="partner1"></li>
                <li class="item"><img :src="partner2"></li>
                <li class="item"><img :src="partner3"></li>
                <li class="item"><img :src="partner4"></li>
                <li class="item"><img :src="partner5"></li>
                <li class="item"><img :src="partner6"></li>
                <li class="item"><img :src="partner7"></li>
                <li class="item"><img :src="partner8"></li>
                <li class="item"><img :src="partner9"></li>
                <li class="item"><img :src="partner10"></li>
                <li class="item"><img :src="partner11"></li>
                <li class="item"><img :src="partner12"></li>
                <li class="item"><img :src="partner13"></li>
                <li class="item"><img :src="partner14"></li>
                <li class="item"><img :src="partner15"></li>
            </ul>
        </div>

        <footer class="footer bg" :style="{'background-image': `url(${footerBg})`}">

            <img class="qrcode" :src="weixin">
            <label class="label">金客拉公众号</label>
            <img class="qrcode" :src="weixin">
            <label class="label">金客拉小程序</label>

            <div class="record">
                <p>北京市海淀区学院路20&nbsp;&nbsp;&nbsp;&nbsp;010-4648946</p>
                <p>京备12321312321</p>
            </div>
        </footer>
    </div>
</template>

<script>
    import recommendBg from '../../static/img/recommendBg.jpg';
    import Phone from '../../static/img/Phone.png';
    import problem from '../../static/img/problem.jpg';

    import Oval1 from '../../static/img/Oval1.png';
    import Oval2 from '../../static/img/Oval2.png';
    import Oval3 from '../../static/img/Oval3.png';
    import Oval4 from '../../static/img/Oval4.png';
    import Oval5 from '../../static/img/Oval5.png';

    import companyBg from '../../static/img/companyBg.png';

    import copy1 from '../../static/img/copy1.png';
    import copy2 from '../../static/img/copy2.png';
    import copy3 from '../../static/img/copy3.png';
    import copy4 from '../../static/img/copy4.png';

    import footerBg from '../../static/img/footerBg.png';

    import weixin from '../../static/img/qrcode-weixin.jpg';
    import xiaochengxu from '../../static/img/qrcode-xiaochengxu.jpg';

    import partner1 from '../../static/img/partner1.png';
    import partner2 from '../../static/img/partner2.png';
    import partner3 from '../../static/img/partner3.png';
    import partner4 from '../../static/img/partner4.png';
    import partner5 from '../../static/img/partner5.png';
    import partner6 from '../../static/img/partner6.png';
    import partner7 from '../../static/img/partner7.png';
    import partner8 from '../../static/img/partner8.png';
    import partner9 from '../../static/img/partner9.png';
    import partner10 from '../../static/img/partner10.png';
    import partner11 from '../../static/img/partner11.png';
    import partner12 from '../../static/img/partner12.png';
    import partner13 from '../../static/img/partner13.png';
    import partner14 from '../../static/img/partner14.png';
    import partner15 from '../../static/img/partner15.png';

    export default {
        data() {
            return {
                recommendBg,
                Phone,
                problem,

                Oval1,
                Oval2,
                Oval3,
                Oval4,
                Oval5,

                companyBg,

                copy1,
                copy2,
                copy3,
                copy4,

                footerBg,

                weixin,
                xiaochengxu,

                partner1,
                partner2,
                partner3,
                partner4,
                partner5,
                partner6,
                partner7,
                partner8,
                partner9,
                partner10,
                partner11,
                partner12,
                partner13,
                partner14,
                partner15,
            };
        },

        created() {

        },

        mounted() {

        },

        methods: {},

        computed: {},

        watch: {},

        components: {},
    }
</script>
