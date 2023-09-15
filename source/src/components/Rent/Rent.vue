<template>
    <section id="rent-scooter" class="container container-rent">
        <div class="container-rent__title">
            Как арендовать самокат
        </div>
        <div class="container-rent__content">
            <div class="container-rent__content_info">
                <div class="container-rent__content_info-step">
                    <img class="container-rent__content_info-image" style="display: block;" src="https://avatars.mds.yandex.net/get-lpc/403342/f97c3e9b-721d-4a02-b144-2e5a0a368654/orig">
                    <div class="container-rent__content_info-text blockquote"></div>
                </div>
                <div class="container-rent__content_info-step">
                    <img style="display: block;" src="https://avatars.mds.yandex.net/get-lpc/1370085/80de62cf-bad2-4b16-ae0a-00f66cf01e80/orig">
                    <div class="container-rent__content_info-text blockquote"></div>
                </div>
                <div class="container-rent__content_info-step">
                    <img class="container-rent__content_info-image" style="display: block;" src="https://avatars.mds.yandex.net/get-lpc/1370085/c0430b62-e7b0-48b2-9f8e-757dcfaee867/orig">
                    <div class="container-rent__content_info-text blockquote"></div>
                </div>
            </div>
            <RentDesktop v-if="isFlag"/>
            <RentMobile v-else/>
        </div>
        <div class="container-rent__content_curve-image"></div>
    </section>
</template>

<script>
import RentDesktop from '@/components/Rent/RentDesktop.vue'
import RentMobile from '@/components/Rent/RentMobile.vue'
import { ref } from '@vue/reactivity';

export default {
    components: {RentDesktop, RentMobile},
    setup() {
        let isFlag = ref(true)
        const funFlag = () => {
            let widthContent = window.screen.width;
            let Flag = (widthContent >= 1024) ? true : false;
            return Flag;
        }
        isFlag = funFlag();
        
        return {
            isFlag
        }
    }
}
</script>