 <template>
	<div class="faqsClass" ref="faqs">
        <div class="faqsImgClass">
			<img src="../assets/faqs/Group14.png"/>
		</div>
        <div>
            <p class="faqsTitleClass">
                FAQ
            </p>
            <p class="faqsTextClass">
                Questions and Answers on Professional Traffic Permits:
            </p>
        </div>
        <div class="questionBoxClass">
            <v-expansion-panels accordion>
                <v-expansion-panel>
                    <v-expansion-panel-header>{{example.question}}</v-expansion-panel-header>
                    <v-expansion-panel-content>
                        {{example.answ}}
                    </v-expansion-panel-content>
                </v-expansion-panel>
            </v-expansion-panels>
        </div>
	</div>
</template>

<script>
export default {
	name: 'Faqs',
    data() {
        return {
            example: {
                question: "What is a professional traffic permit?",
                answ: "Traffic permits are a requirement for conducting professional traffic."
            },
            rowOne : [
                { question: "How to check the traffic condition?",
                    answ: ""},
                { question: "What are the requirements for a professional traffic permit?",
                    answ: ""},
                { question: "Are there professional traffic permit training courses at a distance?",
                    answ: ""}
            ],
            rowTwo : [
                { question: "When is a professional traffic permit needed?",
                    answ: ""},
                { question: "Where to look for a traffic permit?",
                    answ: ""},
                { question: "Are there differences between a traffic permit and a professional traffic permit?",
                    answ: ""},
                { question: "How much does a commercial traffic permit cost for goods?",
                    answ: ""},
                { question: "How to plug in for the traffic permit test?",
                    answ: ""},
                { question: "How is the sample for a professional traffic permit booked?",
                    answ: ""}
            ],
            moreInfo: [
                { question: "", answ: ""},
                { question: "", answ: ""}
            ]
        }
    },
	mounted() {
        // Send the reference to the parent
        this.$emit('reference', 'faqs', this.$refs['faqs']);
	}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
/* @import '../styles/howTo.css'; */
@import url('https://fonts.googleapis.com/css2?family=Rubik:wght@700&display=swap');

@font-face {
	font-family: DmSerifDisplay;
	src: url("../assets/fonts/DMSerifDisplay-Regular.ttf");
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

.faqsTitleClass {
    position: absolute;
    width: 166px;
    height: 50px;
    margin-top: 224px;
    /* text */
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

.faqsTextClass {
    position: absolute;
    width: 550px;
    height: 200px;
    margin-top: 318.16px;
    /* text */
    font-family: DmSerifDisplay;
    font-style: normal;
    font-weight: normal;
    font-size: 48px;
    line-height: 140%;

    color: #402B2B;
}

.questionBoxClass {
    position: absolute;
    width: 1120px;
    height: 812px;
    margin-top: 688px;
}

</style>
