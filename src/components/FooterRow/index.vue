<template>
    <div :class="$style['contact-container']">
        <img 
            :class="$style['contact-img']"
            src="https://www.prismax.be/wp/wp-content/themes/prismax/assets/media/trial.jpg"
        >
        <div :class="$style['contact-info']">
            <span :class="$style['title']">Contact</span>
            <div :class="$style['contact-info-box']">
                <div :class="$style['info-msg']">
                    <div :class="[$style['info-msg-title'], $style['info-reset-msg']]">
                        Prismax
                    </div>
                    <div :class="$style['info-reset-msg']">
                        Schuttersvest 73
                    </div>
                    <div :class="$style['info-reset-msg']">
                        2800 Mechelen, Belgium
                    </div>
                </div>

                <div :class="$style['info-msg']">
                    <div :class="[$style['info-msg-title'], $style['info-reset-msg']]">
                        Contact us
                    </div>
                    <div :class="$style['info-reset-msg']">
                        info@prismax.be
                    </div>
                    <div :class="$style['info-reset-msg']">
                        +32 (0)15 65 97 65
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss" module>
.contact-container {
    position: relative;
    width: 100%;
    height: 700px;
    color: #fff;

    .contact-img {
        position: absolute;
        bottom: 0;
        left: 0;
        z-index: -1;
        width: 100%;
        height: 100%;
    }

    .contact-info {
        position: absolute;
        width: 50%;
        max-width: 500px;
        left: 10%;
        bottom: 50%;
        display: flex;
        flex-direction: column;
        flex-wrap: wrap;
    }
}

.contact-info-box {
    display: flex;
}

.title {
    font-family: "Source Sans Pro Bold",sans-serif;
    font-weight: bold;
    font-size: 3rem;
    margin-bottom: 1em;
}

.info-msg {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    width: 48%;
    padding-right: 2%;

    .info-reset-msg {
        font-size: 1.2rem;
        padding-bottom: 0.4em;
    }

    .info-msg-title {
        color: #4bbfe8;
    }
}
</style>