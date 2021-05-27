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

.aboutUsImg {
    position: absolute;
    width: 575.12px;
    height: 480px;
    margin-left: 595px;
}

.aboutTextBox {
    position: absolute;
    width: 570px;
    height: 476px;
    margin-top: 54px
}

.aboutTitle {
    position: absolute;
    width: 166px;
    height: 50px;

    font-family: Rubik;
    font-style: normal;
    font-weight: bold;
    font-size: 24px;
    line-height: 40px;
    display: flex;
    align-items: center;
    letter-spacing: 0.1em;

    color: #EE4D47;
}

.aboutText {
    position: absolute;
    width: 470px;
    height: 156px;
    margin-top: 124px;
    /* text */
    font-family: Rubik;
    font-style: normal;
    font-weight: 300;
    font-size: 18px;
    line-height: 40px;
    /* text */
    color: #402B2B;
}

.posRect1 {
    position: absolute;
    width: 10px;
    height: 160px;
    margin-top: 336px;
}
.posRect2 {
    position: absolute;
    width: 570px;
    height: 160px;
    margin-top: 336px;
    margin-left: 10px;
}

.aboutQuestion {
    position: absolute;
    width: 460px;
    height: 100px;
    margin-top: 366px;
    margin-left: 65px;
    
    /* text */
    font-family: Rubik;
    font-style: normal;
    font-weight: 500;
    font-size: 24px;
    line-height: 36px;
    
    color: #402B2B;
}
</style>
