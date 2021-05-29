 <template>
	<div class="footerClass" ref="footer">
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
			<button class="aboutMenuBtnClass" @click="goto('about')"> ABOUT </button>
			<button class="howToMenuBtnClass" @click="goto('howToApply')"> HOW TO </button>
			<button class="faqsMenuBtnClass" @click="goto('faqs')"> FAQS </button>
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
		// Send the reference to the parent
        this.$emit('reference', 'footer', this.$refs['footer']);
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
            if (this.name === '') {
                alert("Nothings can be done this way, Hendrik Larsson!");
            } else {
                alert("Nothings can be done this way, " + this.name + "!");
            }
        },
        goto(refName) {
            this.$emit('goto', refName);
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import '../styles/footer.css';
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
</style>
