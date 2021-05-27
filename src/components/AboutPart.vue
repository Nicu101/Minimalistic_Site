<template>
	<div class="about">
        <div class="aboutUsImg">
			<img src="../assets/aboutUs/Illustration.png"/>
		</div>
        <div class="aboutTextBox">
            <p class="aboutTitle">
                ABOUT US
            </p>
            <p class="aboutText">
                The occupational traffic permit is one of the most important things in the company when carrying out freight transport.
                In fact, it is a prerequisite for doing business traffic at all.
            </p>
            <div>
                <img class="posRect1" src="../assets/aboutUs/Rectangle18.png"/>
                <img class="posRect2" src="../assets/aboutUs/Rectangle19.png"/>
                <p class="aboutQuestion">
                    How do you do when you need to obtain a commercial traffic permit for freight transport to your business?
                </p>
            </div>
        </div>
	</div>
</template>

<script>
export default {
	name: 'AboutPart',
	mounted() {
		//console.log(window.scrollY);
	}

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import '../styles/aboutUs.css';

@font-face {
	font-family: Rubik;
	src: url("../assets/fonts/Rubik-Regular.ttf");
}

.about {
    position: absolute;
    width: 1170.8px;
    height: 550px;
    margin-left: 245px;
    margin-top: 1290px;

    mix-blend-mode: normal;
}
</style>
