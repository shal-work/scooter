<template>
    <header class="container-menu">
        <div class="container-menu__nav">
            <div class="row">
                <div class="navbar" >
                    <a href="#map">
                        <span class="container-menu__logo">
                            <div class="logo"></div>
                        </span>
                    </a>
                    <ul class="nav">
                        <li class="active"><a href="#rent-scooter">Как арендовать самокат</a></li>
                        <li><a href="#ticket">Катайтесь с Плюсом</a></li>
                        <li><a href="#warning">Катайтесь аккуратно</a></li>
                        <li><a href="#map">Где самокаты?</a></li>
                    </ul>
                    <div class="nav__actiopn_button" v-if="isFlag">
                        <a href="#qr" class="actiopn_button__text" >
                            Скачать
                        </a>    
                    </div>
                    <div class="nav__actiopn_button" v-else>
                        <a href="#download-app" class="actiopn_button__text">
                            Скачать
                        </a>    
                    </div>
                </div>
            </div>
        </div>
        <a class="marquee" href="https://go.yandex/ru_ru/lp/rides/scooter/tula#app" target="_blank"> 
            <marquee-text :pauseOnHover="true">
                Задача сверстать страницу (десктоп и адаптив) как образце по ссылке...
            </marquee-text>
        </a>
    </header>

</template>

<script>
    import { ref } from 'vue'
	import { Vue3Marquee } from 'vue3-marquee'
    import 'vue3-marquee/dist/style.css'//бегущая строка
	export default {
		components: {'marquee-text' : Vue3Marquee},
		setup() {
            let isFlag = ref(true)
            const funFlag = () => {
                let widthContent = window.screen.width;
                let Flag = (widthContent >= 1700) ? true : false;
                return Flag;
            }
            isFlag = funFlag();
            return {
                isFlag
            }
		},
	}
</script>