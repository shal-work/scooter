<template>
    <section id="warning" class="container-warning">
        <div class="container-warning__block">
            <div class="container-warning__block_title"> </div>
                <WarningDesktop v-if="isFlag"/>
                <WarningMobile v-else/>
        </div>
        <div class="container-warning__insurance">
            <div class="container-warning__insurance_block">
                <img src="https://avatars.mds.yandex.net/get-lpc/1368426/b66b005d-4cd9-4bdc-8737-acb70a4e7801/orig"
                    style="display: block; pointer-events: none; margin-bottom: 24px;">
                <div class="container-warning__insurance_text">
                    Во&nbsp;время поездки на&nbsp;самокате действует страхование жизни и&nbsp;здоровья&nbsp;— вашей
                    и&nbsp;окружающих. Если во&nbsp;время катания что-то произошло, сразу&nbsp;же напишите
                    в&nbsp;поддержку
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import WarningDesktop from '@/components/Warning/WarningDesktop.vue'
import WarningMobile from '@/components/Warning/WarningMobile.vue'
import { ref } from '@vue/reactivity';

export default {
    components: {WarningDesktop, WarningMobile},
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
