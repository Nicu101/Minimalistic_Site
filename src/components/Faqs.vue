 <template>
	<div class="faqsClass">
        <div class="faqsImgClass">
			<img src="../assets/howTo/illustrations.png"/>
		</div>
        <div>
            <p class="faqsTitleClass">
                FAQ
            </p>
            <p class="faqsTextClass">
                Questions and Answers on Professional Traffic Permits:
            </p>
        </div>
	</div>
</template>

<script>
export default {
	name: 'Faqs',
	mounted() {
		//console.log(window.scrollY);
	}

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
/* @import '../styles/howTo.css'; */

@font-face {
	font-family: Rubik;
	src: url("../assets/fonts/Rubik-Regular.ttf");
}

.faqsClass {
    position: absolute;
    width: 1360px;
    height: 1500px;
    margin-left: 240px;
    margin-top: 2799px;

    mix-blend-mode: normal;
    /* Background img */
    background-image: url("../assets/faqs/background.png");
	background-repeat: no-repeat;
    background-position-x: 190px;
}

.faqsImgClass {
    position: absolute;
    width: 708px;
    height: 490.57px;
    margin-left: 475px;
    margin-top: 107.65px;
}
</style>
