 <template>
	<div class="howTo">
        <div class="howToImg">
			<img src="../assets/howTo/illustrations.png"/>
		</div>
        <div>
            <p class="howToTitle">
                How to Apply
            </p>
            <p class="howToText">
                When applying for a traffic permit, there are certain requirements that you must meet that are included in the examination: 
                requirements for professional knowledge, solid establishment, good reputation and financial resources. 
                Important to remember is to confirm your application for a traffic permit by the company's company signer or CEO.
            </p>
        </div>
	</div>
</template>

<script>
export default {
	name: 'HowToPart',
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

.howTo {
    position: absolute;
    width: 1232.61px;
    height: 679px;
    margin-left: 127px;
    margin-top: 2004.81px;

    mix-blend-mode: normal;
}

.howToImg {
    position: absolute;
    width: 720.52px;
    height: 679.39px;
}

.howToTitle {
    position: absolute;
    width: 265px;
    height: 50px;
    margin-left: 777.61px;
    margin-top: 96.19px;
    /* text */
    font-family: Rubik;
    font-style: normal;
    font-weight: bold;
    font-size: 24px;
    line-height: 40px;
    display: flex;
    align-items: center;
    letter-spacing: 0.1em;
    text-transform: uppercase;

    color: #EE4D47;
}

.howToText {
    position: absolute;
    width: 455px;
    height: 287px;
    margin-left: 777.61px;
    margin-top: 186.19px;
    /* text */
    font-family: Rubik;
    font-style: normal;
    font-weight: 300;
    font-size: 18px;
    line-height: 40px;

    color: #402B2B;
}

</style>
