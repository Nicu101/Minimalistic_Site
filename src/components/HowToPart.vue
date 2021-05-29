 <template>
	<div class="howTo" ref="howToApply">
        <div class="howToImg">
            <transition name="howToRunIn">
                <img v-if="animate" src="../assets/howTo/illustrations.png"/>
            </transition>
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
    props: {
        scrollY: scrollY
    },
	mounted() {
        // Send the reference to the parent
		this.$emit('reference', 'howToApply', this.$refs['howToApply']);
	},
    computed: {
        animate() {
            if (this.scrollY > 1300) {
				return true;
			} else {
				return false;
			}
        }
    },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import '../styles/howTo.css';

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
</style>
