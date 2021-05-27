 <template>
	<div class="footerClass">
        <div class="footerImgClass">
            animation
		</div>
        <div>
            
        </div>
	</div>
</template>

<script>
export default {
	name: 'Footer',
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

.footerClass {
    position: absolute;
    width: 1508px;
    height: 909.82px;
    margin-left: -113px;
    margin-top: 4447.18px;
    mix-blend-mode: normal;
    /* Background img */
    background-image: url("../assets/footer/BG.png");
	background-repeat: no-repeat;
    background-position-x: 108px;
    background-position-y: 170.39px;
}
</style>
