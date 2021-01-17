<template>
    <div :class="$style['header-row']">
        <a href="#" :class="$style['nav-img']">
            <img src="https://www.prismax.be/wp/wp-content/themes/prismax/assets/media/logo_prismax_white.svg">
        </a>

        <div :class="$style['nav-btn-box']">
            <a 
                v-for="(item, index) in btnList" 
                :key="index" 
                :href="item.href"
                :class="[$style['nav-btn']]"
            >
                {{ item.name }}
            </a>
        </div>
    </div>
</template>

<script>
    import { reactive, toRefs } from 'vue'
    
    export default {
        setup() {
            const state = reactive({
                btnList: [
                    {name: 'HOME', href: '#home'},
                    {name: 'ABOUT', href: '#about'},
                    {name: 'SHOWREEL', href: '#showreel'},
                    {name: 'WORK', href: '#work'},
                    {name: 'CONTACT', href: '#contact'},
                ]
            })

            return {
                ...toRefs(state)
            }
        }
    }
</script>

<style lang="scss" module>
.header-row {
    position: fixed;
    z-index: 99;
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;
    box-sizing: border-box;
    padding: 2em;
    transition: 0.3s ease;

    .nav-img {
        flex: 1;
        max-width: 140px;
    }

    .nav-btn-box {
        display: inline-flex;
        align-items: center;
        justify-content: center;

        .nav-btn {
            display: inline-block;
            background: rgba(34,31,30,0.8);
            color: #fff;
            font-family: "Source Sans Pro Bold",sans-serif;
            font-size: 1rem;
            text-transform: uppercase;
            padding: 0.8em 1.2em;
            transition: 0.15s ease;
            transform: skewX(-10deg);
            margin: 0 0.1rem;
        }
    }
}

.selected-nav-btn {
    background: rgba(75,191,232,0.8);
}
</style>