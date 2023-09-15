<template>
    <section id="ticket" class="container-ticket">
        <div class="container-ticket__background">
            <div class="container-ticket__content">
                <div class="container-ticket__title">
                    Абонемент на&nbsp;самокаты в&nbsp;Яндекс Плюсе
                </div>
                <div class="container-ticket__text">
                    Если вы&nbsp;часто ездите по&nbsp;городу на&nbsp;самокатах, выгоднее будет с&nbsp;абонементом. Его можно купить, только если у&nbsp;вас есть Яндекс Плюс. Абонемент бесплатный на&nbsp;первый месяц. Вот&nbsp;какие бонусы он&nbsp;даёт:
                </div>
                <img class="pluses-circle" src="https://avatars.mds.yandex.net/get-lpc/1368426/f3f68bd0-fba4-4318-ad1c-2649bd5906ae/orig">
                <TicketDesktop v-if="isFlag"/>
                <TicketMobile v-else/>
            </div>
            <div class="decoration-line"></div>
        </div>
    </section>
</template>

<script>
import TicketDesktop from '@/components/Ticket/TicketDesktop.vue'
import TicketMobile from '@/components/Ticket/TicketMobile.vue'
import { ref } from '@vue/reactivity';

export default {
    components: {TicketDesktop, TicketMobile},
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