<template>
    <section>
        <div id="btn-tariff" class="container container-btn-tariff">
            <div class="container-btn-tariff_text"></div>
        </div>
        <div id="tariff">
            <TariffDesktop v-if="isFlag"/>
            <TariffMobile v-else/>
        </div>
    </section>
</template>


<script>
import TariffDesktop from '@/components/Tariff/TariffDesktop.vue'
import TariffMobile from '@/components/Tariff/TariffMobile.vue'
import { ref } from '@vue/reactivity';

export default {
    components: {TariffDesktop, TariffMobile},
    setup() {
        let isFlag = ref(true)
        const funFlag = () => {
            let widthContent = window.screen.width;
            let Flag = (widthContent >= 767) ? true : false;
            return Flag;
        }
        isFlag = funFlag();
        return {
            isFlag
        }
    }
}
</script>