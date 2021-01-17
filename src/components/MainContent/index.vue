<template>
    <div :class="$style['init']">
        <div :class="$style['main-content']">
            <img 
                src="https://www.prismax.be/wp/wp-content/uploads/2018/10/header-1.jpg"
                :class="$style['main-content-img']"
            >
            <video 
                src="https://www.prismax.be/wp/wp-content/uploads/2020/10/Banner-2020-SHORT-1.mp4"
                :class="$style['main-content-video']"
                autoplay 
                loop 
                muted
            />
        </div>

        <div :class="$style['shape-container']">
            <div :class="$style['section']">
                <div :class="$style['instagram-content']">
                    <div :class="$style['instagram']">
                        <div :class="$style['sb-instagram']">
                            <div :class="$style['sbi-images']">
                                <div 
                                    v-for="(item, index) in instagramImgArr"
                                    :key="index"
                                    :class="$style['sbi-item']"
                                >
                                    <div :class="$style['sbi-photo-wrap']">
                                        <a 
                                            :class="$style['sbi-photo']" 
                                            :href="item.href"
                                        >
                                            <img 
                                                :class="$style['sbi-img']" 
                                                :src="item.url"
                                            >
                                        </a>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <div :class="$style['about-content']">
                    <h1 :class="$style['title']">Hi, we are Prismax</h1>
                    <div>
                        <p :class="$style['content']">
                            Do you want to embellish your event with entertaining visual elements? Prismax is the one stop shop you need.
                        </p>

                        <p :class="$style['content']">
                            We create custom motion graphics, take care of the live operating and offer technical video support.
                        </p>

                        <p :class="$style['content']">
                            From elaborate LED screen setups to projection on buildings, we make it happen.
                        </p>

                        <p :class="$style['content']">
                            With over 15 years of experience, we energize your event beyond expectations.
                        </p>

                        <div :class="$style['social']">
                            <strong :class="$style['social-content']">
                                Like or follow us on
                            </strong>

                            <div :class="$style['social-link-box']">
                                <a 
                                :class="$style['social-link']" 
                                href="https://www.facebook.com/prismaxvj/?fref=ts"
                                >
                                    <div>FB</div>
                                </a>
                                <a 
                                    :class="$style['social-link']" 
                                    href="https://www.instagram.com/accounts/login/"
                                >
                                    <div>IG</div>
                                </a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <svg :class="$style['shape-item']" viewBox="0 0 401 497.64">
                <polygon 
                    :class="$style['part-blue']" 
                    points="55.26 222.54 226.32 55.26 0 0 0 57.02 55.26 222.54" 
                />
                <polygon 
                    :class="$style['part-black']" 
                    points="126.32 432.46 0 57.02 0 497.64 44.74 497.64 126.32 432.46" 
                />
                <polygon 
                    :class="$style['part-blue']"
                    points="400 497.64 126.32 432.46 44.74 497.64 400 497.64"
                />
            </svg>

            <div :class="$style['section-area-img']" />
        </div>

        <div :class="[$style['section'], $style['shapes-section']]">
            <div :class="$style['portfolio-container']">
                <span :class="$style['title']">Portfolio</span>
                <div :class="[$style['portfolio-grid'], $style['alm-listing']]">
                    <div :class="$style['alm-reveal']">
                        <a  
                            v-for="(item, index) in portfolioArr"
                            :key="index"
                            :class="$style['portfolio-item']" 
                            :href="item.href"
                        >
                            <div :class="$style['aspect-ratio']">
                                <img :class="$style['item-img']" :src="item.url">
                                <div :class="$style['center-title']">
                                    <span :class="$style['portfolio-item-title']">
                                        {{ item.name }}
                                    </span>
                                </div>
                            </div>
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import { reactive, toRefs } from 'vue';

    export default {
        setup() {
            const state = reactive({
                instagramImgArr: [
                    {
                        url: 'https://scontent-tpe1-1.cdninstagram.com/v/t51.2885-15/e35/135569591_157489185828286_1932264313183316329_n.jpg?_nc_ht=scontent-tpe1-1.cdninstagram.com&_nc_cat=110&_nc_ohc=aZCKM9cyvD4AX_08SAl&tp=1&oh=ef2cd41f74dc5c00609c699cb0badd2c&oe=602C630B', 
                        href:'https://www.instagram.com/p/CJrg86ApHv4/'
                    },
                    {
                        url: 'https://scontent-tpe1-1.cdninstagram.com/v/t51.2885-15/e35/135776664_394434471787899_2516785090792857694_n.jpg?_nc_ht=scontent-tpe1-1.cdninstagram.com&_nc_cat=103&_nc_ohc=lwyYXx-mvDMAX_24saw&tp=1&oh=f4774aa4e6bd2cf5940c1ec894cdb3ef&oe=602E977B', 
                        href:'https://www.instagram.com/p/CJrg86ApHv4/'
                    },
                    {
                        url: 'https://scontent-tpe1-1.cdninstagram.com/v/t51.2885-15/e35/135411933_3666911200069601_3895895660797137209_n.jpg?_nc_ht=scontent-tpe1-1.cdninstagram.com&_nc_cat=105&_nc_ohc=7VMPQTTsFJ8AX-G21qe&tp=1&oh=9e49c4bc3ebff315eef407addf9caee8&oe=602CCB7A', 
                        href:'https://www.instagram.com/p/CJrg86ApHv4/'
                    },
                    {
                        url: 'https://scontent-tpe1-1.cdninstagram.com/v/t51.2885-15/e35/135762333_245824430241160_2208069058746154385_n.jpg?_nc_ht=scontent-tpe1-1.cdninstagram.com&_nc_cat=104&_nc_ohc=QXj8Olmoz_cAX8vfLRO&tp=1&oh=6d5bbfa813d07f752fee80bf443fd175&oe=602C9035', 
                        href:'https://www.instagram.com/p/CJrg86ApHv4/'
                    },
                ],

                portfolioArr: [
                    {
                        url:'https://www.prismax.be/wp/wp-content/uploads/2019/01/46011106_10156293818034177_8921743037776789504_o.jpg', 
                        href: 'https://www.prismax.be/wp/portfolios/tomorrowland/',
                        name: 'Tomorrowland'
                    },
                    {
                        url:'https://www.prismax.be/wp/wp-content/uploads/2019/01/44083858_1902594056526996_2910362568113520640_o.jpg', 
                        href: 'https://www.prismax.be/wp/portfolios/martin-jensen/',
                        name: 'Martin Jensen'
                    },
                    {
                        url:'https://www.prismax.be/wp/wp-content/uploads/2019/01/pic2-jpg.jpg', 
                        href: 'https://www.prismax.be/wp/portfolios/vogue-arabia-launch-qatar/',
                        name: 'Vogue Arabia launch Qatar'
                    },
                    {
                        url:'https://www.prismax.be/wp/wp-content/uploads/2019/01/TT_TRUMPETS_STILL-0-00-00-00.png', 
                        href: 'https://www.prismax.be/wp/portfolios/timmy-trumpet/',
                        name: 'Timmy Trumpet'
                    },
                    {
                        url:'https://www.prismax.be/wp/wp-content/uploads/2019/01/dvlmsite.jpg', 
                        href: 'https://www.prismax.be/wp/portfolios/dimitri-vegas-like-mike/',
                        name: 'Dimitri Vegas & Like Mike'
                    },
                ]
            })

            return {
                ...toRefs(state)
            }
        }
    }
</script>

<style lang="scss" module>
.init {
    background: #0a0a0a;
}

.main-content {
    position: relative;
    width: 100%;
    height: 100vh;
    background: #000;

    &::after {
        content: '';
        position: absolute;
        top: 0;
        left: 0;
        z-index: 2;
        width: 100%;
        height: 100%;
        background: linear-gradient(to bottom, rgba(75,192,232,0.33) 0%, rgba(75,192,232,0) 28%, rgba(75,192,232,0) 100%);
        filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#544bc0e8', endColorstr='#004bc0e8', GradientType=0);
    }

    .main-content-img {
        position: absolute;
        width: 100%;
        height: 100%;
        object-fit: cover;
        object-position: center center;
    }

    .main-content-video {
        opacity: 0.5;
        position: absolute;
        width: 100%;
        height: 100%;
        object-fit: cover;
        object-position: center center;
    }
}

.shape-container {
    position: relative;

    .section {
        position: relative;
        display: inline-block;
        height: 100%;
        min-height: 100vh;
        width: 100%;
        padding: 10%;
        box-sizing: border-box;
        background-image: url('https://www.prismax.be/wp/wp-content/themes/prismax/assets/media/what-the-hex-dark.png');
    }
}

.instagram-content {
    position: relative;
    margin-top: -15px;
    z-index: 1;
    display: flex;
    width: 40%;
    margin-left: 5%;
    float: left;

    .instagram {
        width: 100%;
        margin: 0 auto;

        .sb-instagram {
            padding-bottom: 30px;
            width: 100%;
            margin: 0 auto;
            padding: 0;
            box-sizing: border-box;

            .sbi-images {
                width: 100%;
                line-height: 0;
                padding: 15px;
                box-sizing: border-box;
            }
        }
    }
}

.about-content {
    position: relative;
    z-index: 2;
    display: flex;
    flex-direction: column;
    width: 45%;
    float: right;
    color: #fff;

    .social {
        margin-top: 3rem;
        display: block;
        font-weight: Bold;

        .social-content {
            font-size: 1.2rem;
            displaY: block;
            padding-bottom: 2rem;
        }

        .social-link-box {
            display: flex;

            .social-link {
                color: #fff;
                font-size: 2rem;
                margin-right: 2.5rem;
            }
        }

    }
}


.sbi-item {
    display: inline-flex;
    width: 50%;
    vertical-align: top;
    zoom: 1;
    max-height: 1000px;
    padding: inherit!important;
    margin: 0!important;
    text-decoration: none;
    opacity: 1;
    overflow: hidden;
    box-sizing: border-box;
    transition: all .5s ease;

    .sbi-photo-wrap {
        position: relative;

        .sbi-photo {
            display: block;
            height: 254.4px;
            text-decoration: none;
            opacity: 1;
            background-image: url('https://scontent-amt2-1.cdninstagram.com/v/t51.29350-15/116007662_620101611979340_4459355596038533745_n.jpg?_nc_cat=105&ccb=2&_nc_sid=8ae9d6&_nc_ohc=uV37D4-wwkwAX-qVPh-&_nc_oc=AQk9qNPPPg8gGruPtsPAesqxmBbtJzp880RCA86O_aiD2AGqVsjnwV_rnyO8S8Qht_A&_nc_ht=scontent-amt2-1.cdninstagram.com&oh=ef79f6c…&oe=5FFD6056');
            background-size: cover;
            background-position: center center;
            background-repeat: no-repeat;

            .sbi-img {
                width: 100%;
                height: auto;
            }
        }
    }
}

.shape-item {
    position: absolute;
    top: -10vh;
    bottom: 0;
    left: 0;
    height: calc(100% + 10vh);

    .part-blue {
        visibility: visible;
        fill: rgba(75,191,232,0.66);
    }

    .part-black {
        visibility: visible;
        fill: #141313;
    }
}

.section-area-img {
    display: inline-block;
    height: 100%;
    min-height: 100vh;
    width: 100%;
    padding: 10%;
    box-sizing: border-box;
    background-image: url('https://scontent-tpe1-1.cdninstagram.com/v/t51.2885-15/e35/37754717_2108640652718790_6238650115830054912_n.jpg?_nc_ht=scontent-tpe1-1.cdninstagram.com&_nc_cat=106&_nc_ohc=dSeZJGl1Rb4AX9seedX&tp=1&oh=5ebaa1734754935275cbff46d3bbbfc5&oe=602C8375');
    background-repeat: no-repeat;
    background-position: 50% 100%;
    background-size: 100%;
}

.title {
    font-family: "Source Sans Pro Bold",sans-serif;
    font-weight: bold;
    font-size: 3rem;
    margin-bottom: 1em;
}

.content {
    font-size: 1.1rem;
    line-height: 1.4em;
    margin-bottom: 0.5rem;
}

.shapes-section {
    overflow: hidden;
    padding: 0;
    background-color: #0a0a0a;
    color: #fff;

    .portfolio-container {
        position: relative;
        z-index: 3;
        text-align: center;
        width: calc(100% - 20%);
        padding: 10%;
        margin-top: 80px;

        .portfolio-grid {
            display: flex;
            flex-wrap: wrap;

            .alm-reveal {
                display: flex;
                flex-wrap: wrap;
                height: auto;
                width: 100%;
                margin-top: 80px;
                opacity: 1;
                outline: none;

                .portfolio-item {
                    position: relative;
                    display: inline-block;
                    width: calc(50% - 15px);
                    margin-bottom: 30px;
                    overflow: hidden;

                    &:nth-child(odd) {
                        margin-right: 15px;
                    }

                    &:nth-child(even) {
                        margin-left: 15px;
                    }
                }
            }
        }

        .alm-listing {
            margin: 0;
            padding: 0;
        }
    }
}

.aspect-ratio {
    position: relative;
    padding-bottom: 56.25%;
    width: 100%;

    .item-img {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        max-width: 100%;
        max-height: 100%;
        object-fit: cover;
        transition: 0.15s ease-in;
    }

    .center-title {
        position: absolute;
        display: flex;
        justify-content: center;
        align-items: center;
        width: 100%;
        height: 100%;

        .portfolio-item-title {
            font-family: "Source Sans Pro Bold",sans-serif;
            color: white;
            font-size: 1.3rem;
            font-weight: bold;
            padding: 12px 24px 14px;
            background: rgba(0,0,0,0.85);
            transition: 0.15s ease-in;
            transform: skewX(-10deg);
        }
    }
}

@media screen and (min-width: 480px){
    .main-content-img {
        display: none;
    }
}
</style>