<style scoped lang="scss">
    .bg{
        background-position: center;
        background-repeat: no-repeat;
        background-size: cover;
    }

    $timerDialog: 15s;

    /*四个动画整体20s*/
    $allTime: 24s;

    /*雷达动画*/
    $timerBig: 2.5s;
    $timerWave: 8s;

    /*名片动画*/
    $timerCard: 4s;

    /*聊天动画*/
    $timerTalk: 8s;

    /*网络动画*/
    $timerNetwork: 8s;

    .home {
        background: #ffffff;

        .header {
            color: #fff;
            height: 0.5rem;
            background: #22272F;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 99;
            border-bottom: 1px solid #979797;

            .logo {
                display: inline-block;
                height: .22rem;
                width: .61rem;
                background-size: contain;
                position: absolute;
                top: .14rem;
                left: .24rem;
            }

            .item{
                float: right;
                display: inline-block;
                line-height: .5rem;
                font-size: .15rem;
                margin-right: .25rem;

                a{
                    color: #fff !important;
                }
            }
        }

        .banner {
            height: 8.83rem;
            color: #FFFFFF;
            background: #000000;
            position: relative;

            .name {
                text-align: center;
                padding-top: 1rem;
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
                top: 2.08rem;
                left: .61rem;
                height: 4.98rem;
                width: 2.53rem;
                display: block;
            }

            .text{
                position: absolute;
                width: 100%;
                top: 7.43rem;
                font-size: .12rem;
                text-align: center;
                line-height: .2rem;
                font-weight: bold;
            }
        }

        .data {
            background: #ffffff;
            height: 2.67rem;
            text-align: center;
            padding: 0 .3rem;

            h3{
                font-size: .2rem;
                padding: .3rem 0 0 0;
            }

            .info{
                display: inline-block;
                width: 50%;
                float: left;
                height: .7rem;
                text-align: center;
                margin-top: .3rem;

                .num{
                    font-size: .38rem;
                    display: block;
                }

                .label{
                    font-size: .13rem;
                    color: #8D8D8D;
                    display: block;
                }
            }
        }

        .recommend {
            height: 7.45rem;

            .title{
                line-height: 1.2rem;
                font-size: .25rem;
                letter-spacing: .15rem;
                text-align: center;
            }

            .phonex{
                width: 2.33rem;
                height: 4.72rem;
                margin: 0 auto;
            }

            .label{
                margin-top: .3rem;
                font-size: .48rem;
                color: #282B31;
                text-align: center;
            }
        }

        .institution {
            height: 10.02rem;
            background: #ffffff;

            .title {
                height: .8rem;
                line-height: .8rem;
                font-size: .25rem;
                letter-spacing: .15rem;
                text-align: center;
            }

            .panel{
                width: 3.22rem;
                margin: 0 auto;
                display: block;
            }
        }

        .capital {
            height: 3.5rem;
            transform: translate3d(0, 0, 0);
            overflow: hidden;
            background: #ffffff;

            .content {
                position: absolute;
                height: 8.55rem;
                top: -2.5rem;
                left: -5.5rem;
                width: 14.4rem;
                transform: scale(.25);

                .radar-panel {
                    position: absolute;
                    top: 0;
                    left: 342px;
                    width: 755px;
                    height: 755px;
                    margin: 0 auto;
                    transform: translateX(0);

                    animation: radarPanel $allTime infinite linear;

                    @keyframes radarPanel {
                        0% {
                            transform: translateX(0);
                        }

                        29% {
                            transform: translateX(0);
                        }

                        32% {
                            transform: translateX(-200%);
                        }

                        100% {
                            transform: translateX(-200%);
                        }
                    }

                    .radar-big {
                        position: absolute;
                        height: 755px;
                        width: 755px;
                        top: 0;
                        left: 0;
                        animation: bigRadar $timerBig infinite linear;

                        @keyframes bigRadar {
                            from {
                                transform: rotate(0deg);
                            }

                            to {
                                transform: rotate(360deg);
                            }
                        }
                    }

                    .radar-min {
                        position: absolute;
                        top: 124px;
                        left: 124px;
                        height: 506px;
                        width: 506px;
                        animation: minRadar $timerBig infinite linear;

                        @keyframes minRadar {
                            from {
                                transform: rotate(0deg);
                            }

                            to {
                                transform: rotate(-360deg);
                            }
                        }
                    }

                    .radar-logo {
                        position: absolute;
                        top: 50%;
                        left: 50%;
                        transform: translate(-50%, -50%);
                        width: 284px;
                        height: 284px;
                    }

                    .radar-wave {
                        position: absolute;
                        top: 0;
                        left: 0;
                        height: 755px;
                        width: 755px;
                        animation: minWave $timerWave infinite linear;

                        @keyframes minWave {
                            from {
                                transform: rotate(0deg);
                            }

                            to {
                                transform: rotate(360deg);
                            }
                        }
                    }

                    .target {
                        position: absolute;
                        background-size: contain;
                        opacity: 0;

                        &.target-1 {
                            top: 0;
                            left: 300px;
                            width: 130px;
                            height: 187px;

                            animation: target1 $timerWave infinite linear;

                            @keyframes target1 {
                                0% {
                                    opacity: 0;
                                }
                                10% {
                                    opacity: 1;
                                }
                                15% {
                                    opacity: 1;
                                }
                                25% {
                                    opacity: 0;
                                }
                                100% {
                                    opacity: 0;
                                }
                            }
                        }

                        &.target-2 {
                            top: 200px;
                            left: 500px;
                            width: 131px;
                            height: 157px;

                            animation: target2 $timerWave infinite linear;

                            @keyframes target2 {
                                0% {
                                    opacity: 0;
                                }
                                15% {
                                    opacity: 0;
                                }
                                25% {
                                    opacity: 1;
                                }

                                30% {
                                    opacity: 1;
                                }
                                40% {
                                    opacity: 0;
                                }
                                100% {
                                    opacity: 0;
                                }
                            }
                        }

                        &.target-3 {
                            top: 400px;
                            left: 600px;
                            width: 181px;
                            height: 157px;

                            animation: target3 $timerWave infinite linear;

                            @keyframes target3 {
                                0% {
                                    opacity: 0;
                                }
                                30% {
                                    opacity: 0;
                                }
                                40% {
                                    opacity: 1;
                                }
                                45% {
                                    opacity: 1;
                                }
                                55% {
                                    opacity: 0;
                                }
                                100% {
                                    opacity: 0;
                                }
                            }
                        }

                        &.target-4 {
                            top: 500px;
                            left: 400px;
                            width: 130px;
                            height: 187px;

                            animation: target4 $timerWave infinite linear;

                            @keyframes target4 {
                                0% {
                                    opacity: 0;
                                }
                                45% {
                                    opacity: 0;
                                }
                                55% {
                                    opacity: 1;
                                }
                                60% {
                                    opacity: 1;
                                }
                                70% {
                                    opacity: 0;
                                }
                                100% {
                                    opacity: 0;
                                }
                            }
                        }

                        &.target-5 {
                            top: 100px;
                            left: 50px;
                            width: 181px;
                            height: 192px;

                            animation: target5 $timerWave infinite linear;

                            @keyframes target5 {
                                0% {
                                    opacity: 0;
                                }
                                75% {
                                    opacity: 0;
                                }
                                80% {
                                    opacity: 1;
                                }
                                95% {
                                    opacity: 1;
                                }
                                100% {
                                    opacity: 0;
                                }
                            }
                        }

                        &.target-6 {
                            top: 500px;
                            left: 0;
                            width: 130px;
                            height: 187px;
                            animation: target6 $timerWave infinite linear;
                            transform: scale(1, 1);

                            @keyframes target6 {
                                0% {
                                    opacity: 0;
                                    transform: scale(1, 1);
                                }
                                60% {
                                    opacity: 0;
                                }
                                65% {
                                    opacity: 1;
                                    transform: scale(1, 1);
                                }
                                67% {
                                    opacity: 1;
                                    transform: scale(1.5, 1.5);
                                }
                                100% {
                                    opacity: 1;
                                    transform: scale(1.5, 1.5);
                                }
                            }
                        }
                    }
                }

                .card-panel {
                    position: absolute;
                    top: 0;
                    left: 342px;
                    width: 755px;
                    height: 755px;
                    margin: 0 auto;
                    transform: translateX(200%);

                    animation: cardPanel $allTime infinite linear;

                    @keyframes cardPanel {
                        0% {
                            transform: translateX(200%);
                        }

                        31% {
                            transform: translateX(200%);
                        }

                        33% {
                            transform: translateX(0);
                        }

                        40% {
                            transform: translateX(0);
                        }

                        43% {
                            transform: translateX(-200%);
                        }

                        100% {
                            transform: translateX(-200%);
                        }
                    }

                    .left-people {
                        position: absolute;
                        left: -100px;
                        top: 200px;
                        width: 270px;
                        height: 270px;
                    }

                    .left-card {
                        position: absolute;
                        left: 0;
                        top: 400px;
                        width: 344px;
                        height: 226px;

                        transform: translateX(0%);
                        animation: card1 $timerCard infinite linear alternate;

                        @keyframes card1 {
                            0% {
                                transform: translateX(0%);
                            }

                            50% {
                                transform: translateX(100%);
                            }

                            100% {
                                transform: translateX(0%);
                            }
                        }
                    }

                    .right-people {
                        position: absolute;
                        right: -100px;
                        top: 250px;
                        width: 134px;
                        height: 143px;
                    }

                    .right-card {
                        position: absolute;
                        right: 0;
                        top: 100px;
                        width: 344px;
                        height: 226px;

                        transform: translateX(0%);
                        animation: card2 $timerCard infinite linear alternate;

                        @keyframes card2 {
                            0% {
                                transform: translateX(0%);
                            }

                            50% {
                                transform: translateX(-100%);
                            }

                            100% {
                                transform: translateX(0%);
                            }
                        }
                    }
                }

                .talk-panel {
                    position: absolute;
                    top: 0;
                    left: 342px;
                    width: 755px;
                    height: 755px;
                    margin: 0 auto;
                    transform: translateX(200%);

                    animation: talkPanel $allTime infinite linear;

                    @keyframes talkPanel {
                        0% {
                            transform: translateX(200%);
                        }

                        40% {
                            transform: translateX(200%);
                        }

                        43% {
                            transform: translateX(0);
                        }

                        66% {
                            transform: translateX(0);
                        }

                        69% {
                            transform: translateX(-200%);
                        }

                        100% {
                            transform: translateX(-200%);
                        }
                    }

                    .left-people {
                        position: absolute;
                        left: -200px;
                        top: 200px;
                        width: 270px;
                        height: 270px;
                    }

                    .right-people {
                        position: absolute;
                        right: -200px;
                        top: 250px;
                        width: 134px;
                        height: 143px;
                    }

                    .talk {
                        position: absolute;
                        transform: translateX(0%);
                        opacity: 0;

                        &.left {
                            left: 70px;
                        }

                        &.right {
                            right: -80px;
                        }

                        &.talk-1 {
                            height: 110px;
                            width: 570px;
                            top: 45px;

                            animation: talk1 $timerTalk infinite linear;

                            @keyframes talk1 {
                                0% {
                                    opacity: 0;
                                }

                                25% {
                                    opacity: 0;
                                }

                                37.5% {
                                    opacity: 1;
                                }

                                100% {
                                    opacity: 1;
                                }
                            }
                        }

                        &.talk-2 {
                            height: 147px;
                            width: 647px;
                            top: 150px;

                            animation: talk2 $timerTalk infinite linear;

                            @keyframes talk2 {
                                0% {
                                    opacity: 0;
                                }

                                37.5% {
                                    opacity: 0;
                                }

                                50% {
                                    opacity: 1;
                                }

                                100% {
                                    opacity: 1;
                                }
                            }
                        }

                        &.talk-3 {
                            height: 110px;
                            width: 423px;
                            top: 285px;

                            animation: talk3 $timerTalk infinite linear;

                            @keyframes talk3 {
                                0% {
                                    opacity: 0;
                                }

                                50% {
                                    opacity: 0;
                                }

                                62.5% {
                                    opacity: 1;
                                }

                                100% {
                                    opacity: 1;
                                }
                            }
                        }

                        &.talk-4 {
                            height: 228px;
                            width: 647px;
                            top: 385px;

                            animation: talk4 $timerTalk infinite linear;

                            @keyframes talk4 {
                                0% {
                                    opacity: 0;
                                }

                                62.5% {
                                    opacity: 0;
                                }

                                75% {
                                    opacity: 1;
                                }

                                100% {
                                    opacity: 1;
                                }
                            }
                        }

                        &.talk-5 {
                            height: 110px;
                            width: 306px;
                            top: 600px;

                            animation: talk5 $timerTalk infinite linear;

                            @keyframes talk5 {
                                0% {
                                    opacity: 0;
                                }

                                75% {
                                    opacity: 0;
                                }

                                87.5% {
                                    opacity: 1;
                                }

                                100% {
                                    opacity: 1;
                                }
                            }
                        }
                    }
                }

                .network-panel {
                    position: absolute;
                    top: 0;
                    left: 342px;
                    width: 755px;
                    height: 755px;
                    margin: 0 auto;
                    transform: translateX(200%);

                    animation: networkPanel $allTime infinite linear;

                    @keyframes networkPanel {
                        0% {
                            transform: translateX(200%);
                        }

                        66% {
                            transform: translateX(200%);
                        }

                        69% {
                            transform: translateX(0);
                        }

                        95% {
                            transform: translateX(0);
                        }

                        98% {
                            transform: translateX(-200%);
                        }

                        100% {
                            transform: translateX(-200%);
                        }
                    }

                    .network {
                        position: absolute;
                        top: 0;
                        left: -100px;
                        width: 729px;
                        height: 839px;
                        z-index: 2;
                    }

                    .line {
                        background: #979797;
                        height: 2px;
                        position: absolute;
                        top: 400px;
                        left: 300px;
                        right: -150px;

                        animation: lineTime $timerNetwork infinite linear;

                        @keyframes lineTime {
                            0% {
                                right: -150px;
                            }
                            100% {
                                right: 200px;
                            }
                        }
                    }

                    .people {
                        position: absolute;
                        right: -200px;
                        top: 350px;
                        width: 134px;
                        height: 143px;

                        animation: peopleTime $timerNetwork infinite linear;

                        @keyframes peopleTime {
                            0% {
                                right: -150px;
                            }
                            100% {
                                right: 100px;
                            }
                        }
                    }
                }
            }
        }

        .evaluate {
            background: #F8F9FA;
            transform: translate3d(0, 0, 0);

            .problem {
                height: 1.83rem;
                border-bottom: 1px solid #E7E8EA;
            }

            .dialog-group {
                position: relative;
                overflow: hidden;
                height: 6.71rem;

                .dialog {
                    position: absolute;
                    transition: 2.5s;
                    transform: translateX(250%);
                    width: 3.56rem;
                    height: 1.22rem;
                    left: .09rem;

                    &.d-1 {
                        transform: translateX(-250%);
                    }

                    &.d-2 {
                        transform: translateX(250%);
                    }

                    &.d-3 {
                        transform: translateX(-250%);
                    }

                    &.d-4 {
                        transform: translateX(250%);
                    }

                    &.fixed-mark {
                        &.d-1 {
                            animation: dialog1 $timerDialog forwards infinite;

                            @keyframes dialog1 {
                                0% {
                                    top: 4.51rem;
                                    transform: translateX(-250%);
                                }
                                17% {
                                    top: 4.51rem;
                                    transform: translateX(0);
                                }
                                34% {
                                    top: 3.2rem;
                                    transform: translateX(0);
                                }
                                51% {
                                    top: 1.79rem;
                                    transform: translateX(0);
                                }
                                68% {
                                    top: .38rem;
                                    transform: translateX(0);
                                }
                                85% {
                                    top: .38rem;
                                    transform: translateX(0);
                                }
                                100% {
                                    top: .38rem;
                                    transform: translateX(-250%);
                                }
                            }
                        }

                        &.d-2 {
                            animation: dialog2 $timerDialog forwards infinite;

                            @keyframes dialog2 {
                                0% {
                                    top: 4.51rem;
                                    transform: translateX(250%);
                                }
                                17% {
                                    top: 4.51rem;
                                    transform: translateX(250%);
                                }
                                34% {
                                    top: 4.51rem;
                                    transform: translateX(0);
                                }
                                51% {
                                    top: 3.2rem;
                                    transform: translateX(0);
                                }
                                68% {
                                    top: 1.79rem;
                                    transform: translateX(0);
                                }
                                85% {
                                    top: 1.79rem;
                                    transform: translateX(0);
                                }
                                100% {
                                    top: 1.79rem;
                                    transform: translateX(250%);
                                }
                            }

                        }

                        &.d-3 {
                            animation: dialog3 $timerDialog forwards infinite;

                            @keyframes dialog3 {
                                0% {
                                    top: 4.51rem;
                                    transform: translateX(-250%);
                                }
                                17% {
                                    top: 4.51rem;
                                    transform: translateX(-250%);
                                }
                                34% {
                                    top: 4.51rem;
                                    transform: translateX(-250%);
                                }
                                51% {
                                    top: 4.51rem;
                                    transform: translateX(0);
                                }
                                68% {
                                    top: 3.2rem;
                                    transform: translateX(0);
                                }
                                85% {
                                    top: 3.2rem;
                                    transform: translateX(0);
                                }
                                100% {
                                    top: 3.2rem;
                                    transform: translateX(-250%);
                                }
                            }

                        }

                        &.d-4 {
                            animation: dialog4 $timerDialog forwards infinite;

                            @keyframes dialog4 {
                                0% {
                                    top: 4.51rem;
                                    transform: translateX(250%);
                                }
                                17% {
                                    top: 4.51rem;
                                    transform: translateX(250%);
                                }
                                34% {
                                    top: 4.51rem;
                                    transform: translateX(250%);
                                }
                                51% {
                                    top: 4.51rem;
                                    transform: translateX(250%);
                                }
                                68% {
                                    top: 4.51rem;
                                    transform: translateX(0);
                                }
                                85% {
                                    top: 4.51rem;
                                    transform: translateX(0);
                                }
                                100% {
                                    top: 4.51rem;
                                    transform: translateX(250%);
                                }
                            }
                        }
                    }

                }

                .input {
                    background-size: contain;
                    position: absolute;
                    bottom: .3rem;
                    left: .17rem;
                    width: 3.38rem;
                    height: .33rem;
                }
            }
        }

        .partner {
            height: 3.26rem;
            display: flex;
            flex-wrap: wrap;
            flex-direction: row;
            justify-content: start;
            padding: .23rem;

            img{
                width: .72rem;
                height: .72rem;
                display: inline-block;
                margin: 0 .05rem;
            }
        }

        .footer {
            height: 7.02rem;
            color: #fff;
            padding-top: .47rem;
            background: #22272F;

            .qrcode{
                display: block;
                width: 1.8rem;
                margin: 0 auto;
            }

            .label{
                display: block;
                text-align: center;
                font-size: .12rem;
                margin: .2rem 0 .3rem 0;
            }

            .record{
                padding-top: .1rem;
                font-size: .14rem;
                text-align: center;

                p{
                    margin-bottom: .05rem;
                }

                .phone{
                    margin-left: .1rem;
                }
            }
        }
    }
</style>

<template>
    <div class="home" id="homeTop">
        <header class="header">
            <span class="logo bg" :style="{'background-image': `url(${logo})`}"></span>
            <span class="item"><a href="#recommend">项目</a></span>
            <span class="item"><a href="#institution">资金</a></span>
            <span class="item"><a href="#capital">人脉</a></span>
            <span class="item"><a href="#partner">关于我们</a></span>
        </header>

        <div class="banner">
            <div class="name">
                <h1 class="title">金客拉</h1>
                <p class="sub-title">让金融更简单</p>
            </div>

            <div class="phone bg" :style="{'background-image': `url(${Phone})`}"></div>

            <div class="text">
                <p>金客拉致力于打造一个基于微信生态的，</p>
                <p>连接金融资产与资金的智能匹配交易平台</p>
                <p>同时提供一套连接金融机构与员工微信端的AI管理工具</p>
            </div>
        </div>

        <div class="data">
            <h3>全领域金融市场动态数据库</h3>

            <div class="info">
                <span class="num">8000+</span>
                <label class="label">业务总量</label>
            </div>
            <div class="info">
                <span class="num">800+</span>
                <label class="label">业务更新速度</label>
            </div>
            <div class="info">
                <span class="num">50000+</span>
                <label class="label">顶尖金融人</label>
            </div>
            <div class="info">
                <span class="num">10000+</span>
                <label class="label">机构数量</label>
            </div>
        </div>

        <div class="recommend bg" id="recommend" ><!--:style="{'background-image': `url(${recommendBg})`}"-->
           <!-- <div class="circle circle-1 bg" :style="{'background-image': `url(${Oval1})`}"></div>
            <div class="circle circle-2 bg" :style="{'background-image': `url(${Oval2})`}"></div>
            <div class="circle circle-3 bg" :style="{'background-image': `url(${Oval3})`}"></div>
            <div class="circle circle-4 bg" :style="{'background-image': `url(${Oval4})`}"></div>
            <div class="circle circle-5 bg" :style="{'background-image': `url(${Oval5})`}"></div>-->

            <h1 class="title">推荐项目</h1>
            <div class="phonex bg" :style="{'background-image': `url(${phonex})`}"></div>
            <div class="label">项目&nbsp;触手可及</div>
        </div>

        <div class="institution" id="institution">
            <h3 class="title bg">机构信息</h3>

            <img class="panel" :src="copy1">
            <img class="panel" :src="copy1">
            <img class="panel" :src="copy1">
            <img class="panel" :src="copy1">
        </div>

        <div class="capital" id="capital">
            <div class="content">
                <div class="radar-panel">
                    <div class="radar-big bg" :style="{'background-image': `url(${radarBig})`}"></div>
                    <div class="radar-min bg" :style="{'background-image': `url(${radarMin})`}"></div>

                    <div class="target target-1 bg" :style="{'background-image': `url(${target1})`}"></div>
                    <div class="target target-2 bg" :style="{'background-image': `url(${target2})`}"></div>
                    <div class="target target-3 bg" :style="{'background-image': `url(${target3})`}"></div>
                    <div class="target target-4 bg" :style="{'background-image': `url(${target4})`}"></div>
                    <div class="target target-5 bg" :style="{'background-image': `url(${target5})`}"></div>
                    <div class="target target-6 bg" :style="{'background-image': `url(${target6})`}"></div>

                    <div class="radar-wave bg" :style="{'background-image': `url(${radarWave})`}"></div>
                    <div class="radar-logo bg" :style="{'background-image': `url(${radarLogo})`}"></div>
                </div>

                <div class="card-panel">
                    <span class="left-people bg" :style="{'background-image': `url(${radarLogo})`}"></span>
                    <span class="left-card bg" :style="{'background-image': `url(${card1})`}"></span>

                    <span class="right-people bg" :style="{'background-image': `url(${target6})`}"></span>
                    <span class="right-card bg" :style="{'background-image': `url(${card2})`}">></span>
                </div>

                <div class="talk-panel">
                    <span class="left-people bg" :style="{'background-image': `url(${radarLogo})`}"></span>

                    <span class="talk left talk-1  bg" :style="{'background-image': `url(${talk1})`}"></span>
                    <span class="talk right talk-2 bg" :style="{'background-image': `url(${talk2})`}"></span>
                    <span class="talk left talk-3  bg" :style="{'background-image': `url(${talk3})`}"></span>
                    <span class="talk right talk-4 bg" :style="{'background-image': `url(${talk4})`}"></span>
                    <span class="talk left talk-5 bg" :style="{'background-image': `url(${talk5})`}"></span>

                    <span class="right-people bg" :style="{'background-image': `url(${target6})`}"></span>
                </div>

                <div class="network-panel">
                    <span class="network bg" :style="{'background-image': `url(${network})`}"></span>
                    <span class="line"></span>
                    <span class="people bg" :style="{'background-image': `url(${target6})`}"></span>
                </div>
            </div>
        </div>

        <div class="evaluate">
            <div class="problem bg" :style="{'background-image': `url(${problem})`}"></div>

            <div class="dialog-group" id="dialogGroup">
                <div class="dialog d-1 bg" :class="{'fixed-mark': dFixed}" :style="{'background-image': `url(${review1})`}"></div>
                <div class="dialog d-2 bg" :class="{'fixed-mark': dFixed}" :style="{'background-image': `url(${review2})`}"></div>
                <div class="dialog d-3 bg" :class="{'fixed-mark': dFixed}" :style="{'background-image': `url(${review3})`}"></div>
                <div class="dialog d-4 bg" :class="{'fixed-mark': dFixed}" :style="{'background-image': `url(${review4})`}"></div>

                <div class="input bg" :style="{'background-image': `url(${input})`}"></div>
            </div>
        </div>

        <div class="partner" id="partner">
           <img class="item" :src="partner1">
           <img class="item" :src="partner2">
           <img class="item" :src="partner3">
           <img class="item" :src="partner4">
           <img class="item" :src="partner5">
           <img class="item" :src="partner6">
           <img class="item" :src="partner7">
           <img class="item" :src="partner8">
           <img class="item" :src="partner9">
           <img class="item" :src="partner10">
           <img class="item" :src="partner11">
           <img class="item" :src="partner12">
           <img class="item" :src="partner13">
           <img class="item" :src="partner14">
           <img class="item" :src="partner15">
        </div>

        <footer class="footer bg">

            <img class="qrcode" :src="weixin">
            <label class="label">金客拉公众号</label>
            <img class="qrcode" :src="xiaochengxu">
            <label class="label">金客拉小程序</label>

            <div class="record">
                <p>北京金客科技有限公司</p>
                <p>北京市海淀区学院路20号院北教楼一层117号</p>
                <p>general@linkfinancier.com <span class="phone">010-59418080</span></p>
                <p>网站备案：京ICP备17022003号-1</p>
            </div>
        </footer>
    </div>
</template>

<script>
    import Phone from '../../static/img/Phone.png';
    import problem from '../../static/img/problem.jpg';


    import copy1 from '../../static/img/copy1.png';
    import copy2 from '../../static/img/copy2.png';
    import copy3 from '../../static/img/copy3.png';
    import copy4 from '../../static/img/copy4.png';


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

    import phonex from '../../static/img/phonex.png';

    import review1 from '../../static/img/review1.png';
    import review2 from '../../static/img/review2.png';
    import review3 from '../../static/img/review3.png';
    import review4 from '../../static/img/review4.png';

    import target1 from '../../static/img/target1.png';
    import target2 from '../../static/img/target2.png';
    import target3 from '../../static/img/target3.png';
    import target4 from '../../static/img/target4.png';
    import target5 from '../../static/img/target5.png';
    import target6 from '../../static/img/target6.png';

    import network from '../../static/img/network.png';

    import radarLogo from '../../static/img/radarLogo.png';
    import radarBig from '../../static/img/radarBig.png';
    import radarMin from '../../static/img/radarMin.png';
    import radarWave from '../../static/img/radarWave.png';

    import logo from '../../static/img/logo.png';
    import talk1 from '../../static/img/talk1.png';
    import talk2 from '../../static/img/talk2.png';
    import talk3 from '../../static/img/talk3.png';
    import talk4 from '../../static/img/talk4.png';
    import talk5 from '../../static/img/talk5.png';

    import card1 from "../../static/img/card1.png"
    import card2 from "../../static/img/card2.png"
    import input from "../../static/img/input.png"

    export default {
        data() {
            return {
                phonex,
                Phone,
                problem,


                copy1,
                copy2,
                copy3,
                copy4,

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

                review1,
                review2,
                review3,
                review4,

                dFixed: false,

                target1,
                target2,
                target3,
                target4,
                target5,
                target6,
                network,

                radarLogo,
                radarBig,
                radarMin,
                radarWave,

                card1,
                card2,
                logo,
                input,
                talk1,
                talk2,
                talk3,
                talk4,
                talk5,
            };
        },

        created() {
            const scroll = () => {
                const scrollTop = document.documentElement.scrollTop || document.body.scrollTop;

                if (scrollTop > 550) {
                    this.dFixed = true;
                }
            };
            scroll();

            window.addEventListener("scroll", scroll);
        },

        mounted() {

        },

        methods: {},

        computed: {},

        watch: {},

        components: {},
    }
</script>
