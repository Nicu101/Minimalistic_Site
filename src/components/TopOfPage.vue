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
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@font-face {
	font-family: DmSerifDisplay;
	src: url("../assets/fonts/DMSerifDisplay-Regular.ttf");
}
@font-face {
	font-family: Rubik;
	src: url("../assets/fonts/Rubik-Regular.ttf");
}

.top {
	width: 1734px;
	height: 1005.12px;
	position: absolute;
	margin-top: -14px;
	margin-left: -8px;
	mix-blend-mode: color;
	background-image: url("../assets/top/topBackgroundImg.png");
	background-repeat: no-repeat;
}

.topLogoImg {
	position: absolute;
	width: 212px;
	height: 50px;
	margin-top: 50px;
	margin-left: 240px;
	fill: Solid #FFFFFF;
}

.topMenuBar {
	position: absolute;
	width: 604px;
	height: 60px;
	margin-top: 50px;
	margin-left: 744px;
}

.aboutMenuBtn {
	position: absolute;
	width: 59px;
	height: 19px;
	margin-top: 11px;
	/* Text properties */
	font-family: Rubik;
	font-weight: 700;
	font-style: normal;
	font-size: 16px;
	line-height: 19px;
	line-height: 100%;
	letter-spacing: 5%;
	align-content: center;
	vertical-align: center;
	color: #FFFFFF;
	border: none;
	background: none;
}

.howToMenuBtn {
	position: absolute;
	width: 75px;
	height: 19px;
	margin-top: 11px;
	margin-left: 156px;
	/* Text properties */
	font-family: Rubik;
	font-weight: 700;
	font-style: normal;
	font-size: 16px;
	line-height: 19px;
	line-height: 100%;
	letter-spacing: 5%;
	align-content: center;
	vertical-align: center;
	color: #FFFFFF;
	border: none;
	background: none;
}

.faqsMenuBtn {
	position: absolute;
	width: 59px;
	height: 19px;
	margin-top: 11px;
	margin-left: 325px;
	/* Text properties */
	font-family: Rubik;
	font-weight: 700;
	font-style: normal;
	font-size: 16px;
	line-height: 19px;
	line-height: 100%;
	letter-spacing: 5%;
	align-content: center;
	vertical-align: center;
	color: #FFFFFF;
	border: none;
	background: none;
}

.contactMenuBtn {
	position: absolute;
	width: 158px;
	height: 55px;
	margin-left: 446px;
	/* Text properties */
	font-family: Rubik;
	font-weight: 700;
	font-style: normal;
	font-size: 16px;
	line-height: 19px;
	line-height: 100%;
	letter-spacing: 5%;
	letter-spacing: 1.5px;
	align-content: center;
	vertical-align: center;
	color: #FFFFFF;
	background-color: #EE4D47;
	fill: Solid #EE4D47;
	border: none;
	border-radius: 5px;
}

.topTextBox {
	position: absolute;
	width: 741px;
	height: 300px;
	margin-top: 190px;
	margin-left: 240px;
	color: #FFFFFF;
	font-family: DmSerifDisplay;
	font-weight: 400;
	font-style: normal;
	font-size: 100px;
	line-height: 100px;
	line-height: 100%;
	align-content: Left;
	vertical-align: center;
	fill: Solid #FFFFFF;
}

.GetStartedBtn {
	width: 220px;
	height: 60px;
	position: relative;
	margin-top: 550px;
	margin-left: 240px;
	color: #FFFFFF;
	background-color: #EE4D47;
	fill: Solid #EE4D47;
	border: none;
	border-radius: 5px;
}

.GetStartedBtnText {
	font-family: Rubik;
	font-weight: 700;
	font-style: bold;
	font-size: 16px;
	align-content: left;
	line-height: 18.9px;
	line-height: 100%;
	letter-spacing: 5%;
	letter-spacing: 1.5px;
	padding: 0;
}

.GetStartedBtnImg {
	width: 29.5px;
	height: 12.35px;
	margin-left: 24px;
	motion-rotation: 0deg;
}

.modelTopCar {
	width: 650px;
	height: 430.46px;
	margin-top: 180.81px;
	margin-left: -40px;
}
</style>
