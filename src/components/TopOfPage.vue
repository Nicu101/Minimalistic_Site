<template>
	<div class="top">
		<div class="topLogoImg">
			<img src="../assets/top/topLogoImg.png"/>
		</div>
		<div class="topMenuBar">
			<button class="aboutMenuBtn" @click="goto('about')"> ABOUT </button>
			<button class="howToMenuBtn" @click="goto('howToApply')"> HOW TO </button>
			<button class="faqsMenuBtn" @click="goto('faqs')"> FAQS </button>
			<button class="contactMenuBtn" @click="goto('footer')"> CONTACT US </button>
		</div>
		<div>
			<p class="topTextBox"> Your awesome traffic permit consultant.</p>
		</div>
		<div>
			<button class="GetStartedBtn" @click="goto('footer')">
				<span class="GetStartedBtnText"> GET STARTED </span> 
				<img class="GetStartedBtnImg" src="../assets/top/union.png"/>
			</button>
		</div>
		<div class="modelTopCar">
			<transition name="topRunIn">
				<img v-if="animate" src="../assets/top/mobelTopCar.png"/>
			</transition>
		</div>
	</div>
</template>

<script>
export default {
	name: 'TopOfPage',
	props: {
		scrollY: Number
	},
	computed: {
		animate() {
			if (this.scrollY > 50) {
				return true;
			} else {
				return false;
			}
		}
	},
	methods: {
		goto(refName) {
			this.$emit('goto', refName);
		}
	}

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import '../styles/topOfPage.css';

@font-face {
	font-family: DmSerifDisplay;
	src: url("../assets/fonts/DMSerifDisplay-Regular.ttf");
}
@font-face {
	font-family: Rubik;
	src: url("../assets/fonts/Rubik-Regular.ttf");
}

.top {
	position: absolute;
	width: 1734px;
	height: 1005.12px;
	margin-top: -14px;
	margin-left: -8px;

	mix-blend-mode: normal;
	background-image: url("../assets/top/topBackgroundImg.png");
	background-repeat: no-repeat;
}
</style>
