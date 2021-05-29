<template>
	<div id="app">
		<TopOfPage :scrollY="scrollY" @goto="goto"/>
		<AboutPart :scrollY="scrollY" @reference="getReference"/>
		<HowToPart :scrollY="scrollY" @reference="getReference"/>
		<Faqs @reference="getReference"/>
		<Footer :scrollY="scrollY" @reference="getReference" @goto="goto"/>
	</div>
</template>

<script>
import TopOfPage from './components/TopOfPage.vue'
import AboutPart from './components/AboutPart.vue'
import HowToPart from './components/HowToPart.vue'
import Faqs from './components/Faqs.vue'
import Footer from './components/Footer'

export default {
	name: 'App',
	data() {
		return {
			references: [],
			scrollY: 0,
		}
	},
	created() {
		window.addEventListener('scroll', () => {
			this.scrollY = window.scrollY;
		});
	},
	methods: {
		/* Get the ref from a component */
		getReference(refName, ref) {
			this.references[refName] = ref;
		},
		/* Go to the specified part of the page*/
		goto(refName) {
			/* console.log("Ref name:  " + refName + "\n");
			console.log(this.references); */
			var element = this.references[refName];
			var top = element.offsetTop;

			window.scrollTo(0, top);
		}
	},
	components: {
		TopOfPage,
		AboutPart,
		HowToPart,
		Faqs,
		Footer
	}
}
</script>

<style>
#app {
	background-color: #E5E5E5;
}
</style>
