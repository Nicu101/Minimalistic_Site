<template>
	<div class="top">
		<div class="topLogoImg">
			<img src="../assets/top/topLogoImg.png"/>
		</div>
		<div class="topMenuBar">
			<button class="aboutMenuBtn"> ABOUT </button>
			<button class="howToMenuBtn"> HOW TO </button>
			<button class="faqsMenuBtn"> FAQS </button>
			<button class="contactMenuBtn"> CONTACT US </button>
		</div>
		<div>
			<p class="topTextBox"> Your awesome traffic permit consultant.</p>
		</div>
		<div>
			<button class="GetStartedBtn">
				<span class="GetStartedBtnText"> GET STARTED </span> 
				<img class="GetStartedBtnImg" src="../assets/top/union.png"/>
			</button>
		</div>
		<div>
			<img class="modelTopCar" src="../assets/top/mobelTopCar.png"/>
		</div>
	</div>
</template>

<script>
export default {
	name: 'TopOfPage',
	mounted() {
		//console.log(window.scrollY);
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
