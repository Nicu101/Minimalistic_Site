 <template>
	<div class="footerClass">
        <img class="backgroundImgClass" src="../assets/footer/Vector13.png"/>
        <div class="footerImgBoxClass">
            <img class="trekmobilBackgroundImg1" src="../assets/footer/Vector.png"/>
            <img class="treckmobilImgClass" src="../assets/footer/trekmobil.png"/>
            <img class="trekmobilBackgroundImg2" src="../assets/footer/Vector2.png"/>
		</div>
        <div class="footerBoxClass">
            <img class="footerTextHighliterImgClass" src="../assets/footer/Rectangle18.png"/>
            <p class="footerFormTextClass">
                We provide traffic management consultants so you get started quickly, contact us for a quote today!
            </p>
            <form class="footerFormBoxClass">
                <label class="footerFormNameClass">Name</label>
                <input class="footerFormNameInputClass" id="footerFormName" v-model="name" placeholder="Hendrik Larsson"/>
                <label class="footerFormEmailClass" for="footerFormEmail">Email address</label>
                <input class="footerFormEmailInputClass" id="footerFormEmail" v-model="email" placeholder="Your email address"/>
            </form>
            <button class="footerGetStartedBtnClass" @click="getStarted">
                <p class="GetStartedBtnTextClass"> GET STARTED </p> 
                <img class="GetStartedBtnImgClass" src="../assets/top/union.png"/>
            </button>
        </div>

        <img class="footerLogoClass" src="../assets/footer/logoFooter.png"/>
        <div class="footerMenuBarClass">
			<button class="aboutMenuBtnClass"> ABOUT </button>
			<button class="howToMenuBtnClass"> HOW TO </button>
			<button class="faqsMenuBtnClass"> FAQS </button>
		</div>
        <p class="footerNoteClass">Copyright @ 2019</p>
        <div class="footerSocialLinksClass">
            <a class="facebookLinkClass" href="https://www.facebook.com/">
                <img src="../assets/footer/f.png"/>
            </a>
			<a class="twitterLinkClass" href="https://twitter.com/?lang=en">
                <img src="../assets/footer/t.png"/>
            </a>
			<a class="instagramLinkClass" href="https://www.instagram.com/">
                <img src="../assets/footer/i.png"/>
            </a>
        </div>
	</div>
</template>

<script>
export default {
	name: 'Footer',
	mounted() {
		//console.log(window.scrollY);
	},
    data: function() {
        return {
            name: '',
            email: '',
        }
    },
    methods: {
        getStarted() {
            //do somenthing?
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Rubik:wght@700&display=swap');

@font-face {
	font-family: RubikNormal;
	src: url("../assets/fonts/Rubik-Regular.ttf");
}

.footerClass {
    position: absolute;
    width: 1508px;
    height: 909.82px;
    margin-left: -123px;
    margin-top: 4447.18px;
    mix-blend-mode: normal;
    /* Background img */
    background-image: url("../assets/footer/BG.png");
	background-repeat: no-repeat;
    background-size: 1400px 661.52px;
    background-position-x: 108px;
    background-position-y: 170.39px;
}

.backgroundImgClass {
    position: absolute;
    margin-left:  108px;
    margin-top: 170px;
    opacity: 0.8;
    mix-blend-mode: normal;
}

/***** Treckmobil and his Surroundings *****/
.footerImgBoxClass {
    position: absolute;
    width: 489.2px;
    height: 209.48px;
}

.trekmobilBackgroundImg1 {
    position: absolute;
    width: 189.48px;
    height: 94.38px;
    margin-left: 299.72px; /* 186.72px; */
    margin-top: 93.23px;
}

.trekmobilBackgroundImg2 {
    position: absolute;
    width: 131.03px;
    height: 93.23px;
    margin-left: 105px;
    margin-top: 112.8px;
}

.treckmobilImgClass {
    position: absolute;
    margin-left: 113px;
}
/***** Form box *****/ 
.footerBoxClass {
    position: absolute;
    width: 1025px;
    height: 440px;
    margin-left: 348px;
    margin-top: 49.82px;
}

.footerTextHighliterImgClass {
    position: absolute;
    width: 10px;
    height: 160px;
    margin-top: 210px;
}

.footerFormTextClass {
    position: absolute;
    width: 330px;
    height: 140px;
    margin-top: 220px;
    margin-left: 50px;
    /* text */
    font-family: RubikNormal;
    font-style: 330px;
    font-weight: normal;
    font-size: 20px;
    line-height: 30px;
    display: flex;
    align-items: center;

    color: #FFFFFF;
}

.footerFormBoxClass {
    position: absolute;
    width: 550px;
    height: 440px;
    margin-left: 475px;

    background: #FFFFFF;
    box-shadow: 0px 20px 40px
        rgba(238, 77, 71, 0.1);
    border-radius: 10px;
}

.footerFormNameClass {
    position: absolute;
    width: 95px;
    height: 38px;
    margin-left: 75px;
    margin-top: 52px;
    /* text */
    font-family: RubikNormal;
    font-style: normal;
    font-weight: 50;
    font-size: 16px;
    line-height: 40px;

    color: #402B2B;
}

.footerFormNameInputClass {
    position: absolute;
    width: 400px;
    height: 60px;
    margin-left: 75px;
    margin-top: 100px;
    /* input box */
    background: #FFFFFF;
    border: 2px solid #EE4d47;
    box-sizing: border-box;
    box-shadow: 0px 20px 40px 0px rgba(238, 77, 71, 0.1);
    border-radius: 5px;
    /* text */
    font-family: Rubik;
    font-style: normal;
    font-weight: bold;
    font-size: 18px;
    line-height: 40px;
    padding: 11px 40px;

    color: #402B2B;
}

.footerFormEmailClass {
    position: absolute;
    width: 189px;
    height: 38px;
    margin-left: 75px;
    margin-top: 190px;
    /* text */
    font-family: RubikNormal;
    font-style: normal;
    font-weight: 300px;
    font-size: 16px;
    line-height: 40px;

    color: #402B2B;
}

.footerFormEmailInputClass {
    position: absolute;
    width: 400px;
    height: 60px;
    margin-left: 75px;
    margin-top: 238px;
    /* input box */
    background: #FFFFFF;
    border: 1px solid rgba(238, 77, 71, 0.5);
    box-sizing: border-box;
    border-radius: 5px;
    /* text */
    font-family: RubikNormal;
    font-style: normal;
    font-weight: 300;
    font-size: 18px;
    line-height: 40px;
    padding: 11px 40px;

    color: #402B2B;
}
/*** Get Started button ***/
.footerGetStartedBtnClass {
    position: absolute;
    width: 220px;
    height: 60px;
    margin-left: 550px;
    margin-top: 328px;

    color: #FFFFFF;
    background-color: #EE4D47;
    border: none;
	border-radius: 5px;
}
.footerGetStartedBtnClass:hover {
    background-color: #ce251f;
}

.GetStartedBtnTextClass {
    width: 120px;
    height: 19px;
    margin-left: 23px;
    margin-top: 18px;
    /* text */
    font-family: Rubik;
    font-style: normal;
    font-weight: bold;
    font-size: 16px;
    line-height: 19px;
    display: flex;
    align-items: center;
    letter-spacing: 0.05em;
    text-transform: uppercase;
    text-shadow: rgba(238, 77, 71, 0.1);

    color: #FFFFFF;
}

.GetStartedBtnImgClass {
    position: absolute;
    width: 29.5px;
    height: 12.35px;
    margin-left: 56px;
    margin-top: -33px;
}
/*** Img Logo ***/
.footerLogoClass {
    position: absolute;
    margin-left: 348px;
    margin-top: 659px
}
/***** Footer Menu *****/
.footerMenuBarClass{
    position: absolute;
    width: 368px;
    height: 19px;
    margin-left: 999px;
    margin-top: 670px
}

.aboutMenuBtnClass {
    position: absolute;
    width: 56px;
    height: 19px;
	/* Text properties */
	font-family: Rubik;
	font-weight: normal;
	font-style: normal;
	font-size: 16px;
	line-height: 19px;
	display: flex;
    align-items: center;
    text-align: center;
	letter-spacing: 0.05em;
	text-transform: uppercase;
    /* Eliminating button bacground */
	color: #FFFFFF;
	border: none;
	background: none;
}

.howToMenuBtnClass {
    position: absolute;
    width: 75px;
    height: 19px;
    margin-left: 156px;
	/* Text properties */
	font-family: Rubik;
	font-weight: normal;
	font-style: normal;
	font-size: 16px;
	line-height: 19px;
	display: flex;
    align-items: center;
    text-align: center;
	letter-spacing: 0.05em;
	text-transform: uppercase;
    /* Eliminating button bacground */
	color: #FFFFFF;
	border: none;
	background: none;
}

.faqsMenuBtnClass {
    position: absolute;
    width: 56px;
    height: 19px;
    margin-left: 325px;
	/* Text properties */
	font-family: Rubik;
	font-weight: normal;
	font-style: normal;
	font-size: 16px;
	line-height: 19px;
	display: flex;
    align-items: center;
    text-align: center;
	letter-spacing: 0.05em;
	text-transform: uppercase;
    /* Eliminating button bacground */
	color: #FFFFFF;
	border: none;
	background: none;
}
/*** Footer Note ***/
.footerNoteClass {
    position: absolute;
    width: 465px;
    height: 40px;
    margin-left: 348px;
    margin-top: 869.82px;
    /* text */
    font-family: RubikNormal;
    font-style: normal;
    font-weight: 300;
    font-size: 16px;
    line-height: 30px;
    display: flex;
    align-items: center;

    color: #402B2B;
}
/***** Social Media Links *****/
.footerSocialLinksClass {
    position: absolute;
    width: 170px;
    height: 36px;
    margin-left: 1203px;
    margin-top: 871.82px;
    padding-bottom: 25px;
}

.facebookLinkClass {
    position: absolute;
}

.twitterLinkClass {
    position: absolute;
    margin-left: 67px;
}

.instagramLinkClass {
    position: absolute;
    margin-left: 134px;
}
</style>
