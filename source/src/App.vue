<template>
		<MenuNav/>
		<Intro/>
		<Download/>
		<Links/>
		<Rent/>
		<Tariff/>
		<Ticket/>
		<VideoConmponent/>
		<Warning/>
		<MapConmponent/>
		<FooterConmponent/>
</template>

<script>
	import MenuNav from '@/components/MenuNav/MenuNav'
	import Intro from '@/components/Intro/Intro'
	import Download from '@/components/Download/Download'
	import Links from '@/components/Links/Links'
	import Rent from '@/components/Rent/Rent'
	import Tariff from '@/components/Tariff/Tariff'
	import Ticket from '@/components/Ticket/Ticket'
	import VideoConmponent from '@/components/VideoConmponent/VideoConmponent'
	import Warning from '@/components/Warning/Warning'
	import MapConmponent from '@/components/MapConmponent/MapConmponent'
	import FooterConmponent from '@/components/FooterConmponent/FooterConmponent'
	import '@/components/js/lib.js'
	import '@/components/js/screen.js'


	export default {
		components: {MenuNav, Intro, Download, Links, Rent, Tariff, Ticket, VideoConmponent, Warning, MapConmponent, FooterConmponent},
		setup() {

		},
	}
</script>