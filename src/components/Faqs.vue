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
        <div class="questionBox1Class">
            <v-expansion-panels
                v-model="panel"
                :flat="true"
                >
                <v-expansion-panel class="noBackground">
                    <v-expansion-panel-header class="panelClickedHeaderClass"
                        hide-actions
                        disabled
                        >
                        <p class="headerTextClass">{{example.question}}</p>
                    </v-expansion-panel-header>
                    <v-expansion-panel-content class="panelContentClass">
                        {{example.answ}}
                    </v-expansion-panel-content>
                </v-expansion-panel>
            </v-expansion-panels>
            <div class="whiteSpaceClass"/>
            <v-expansion-panels
                :flat="true"
                >
                <div class="gridClass">
                    <v-expansion-panel
                        v-for="info in rowOne" :key="info.question"
                        class="noBackground"
                        >
                        <v-expansion-panel-header :class="info.class"
                            @click="panelHeaderClassForRow1(info)"
                            hide-actions
                            >
                            <p class="headerTextClass">{{info.question}} </p>
                        </v-expansion-panel-header>
                        <v-expansion-panel-content class="panelContentClass">
                            {{info.answ}}
                        </v-expansion-panel-content>
                    </v-expansion-panel>
                </div>
            </v-expansion-panels>
        </div>

        <div class="questionBox2Class">
            <v-expansion-panels
                :flat="true"
                >
                <div class="gridClass">
                    <v-expansion-panel
                        v-for="info in rowTwo" :key="info.question"
                        class="noBackground"
                        >
                        <v-expansion-panel-header
                            :class="info.class"
                            @click="panelHeaderClassForRow2(info)"
                            hide-actions
                            >
                            <p class="headerTextClass">{{info.question}} </p>
                        </v-expansion-panel-header>
                        <v-expansion-panel-content class="panelContentClass">
                            {{info.answ}}
                        </v-expansion-panel-content>
                    </v-expansion-panel>

                    <v-expansion-panel :class="loadPanelClass"
                        >
                        <div class="loadPanelTextClass">{{message}}</div>
                        <v-expansion-panel-header
                            class="panelLoadClass"
                            hide-actions
                            @click="loadMoreQuestions()"
                            >
                        </v-expansion-panel-header>
                    </v-expansion-panel>
                </div>
            </v-expansion-panels>
        </div>
	</div>
</template>

<script>
export default {
	name: 'Faqs',
    data() {
        return {
            panel: 0,
            example: {
                question: "What is a professional traffic permit?",
                answ: "Traffic permits are a requirement for conducting professional traffic."
            },
            rowOne : [
                { question: "How to check the traffic condition?",
                    answ: "",
                    class: 'panelHeaderClass'
                    },
                { question: "What are the requirements for a professional traffic permit?",
                    answ: "",
                    class: 'panelHeaderClass'
                    },
                { question: "Are there professional traffic permit training courses at a distance?",
                    answ: "",
                    class: 'panelHeaderClass'
                    }
            ],
            rowTwo : [
                { question: "When is a professional traffic permit needed?",
                    answ: "",
                    class: 'panelHeaderClass'
                    },
                { question: "Where to look for a traffic permit?",
                    answ: "",
                    class: 'panelHeaderClass'
                    },
                { question: "Are there differences between a traffic permit and a professional traffic permit?",
                    answ: "",
                    class: 'panelHeaderClass'
                    },
                { question: "How much does a commercial traffic permit cost for goods?",
                    answ: "",
                    class: 'panelHeaderClass'
                    },
                { question: "How to plug in for the traffic permit test?",
                    answ: "",
                    class: 'panelHeaderClass'
                    },
                { question: "How is the sample for a professional traffic permit booked?",
                    answ: "",
                    class: 'panelHeaderClass'
                    }
            ],
            message: 'LOAD MORE',
            loadPanelClass: 'customBackgroundOneClass',
            moreInfo: [
                { question: "What should you do?",
                    answ: "Contact me for more information.",
                    class: 'panelHeaderClass'},
                { question: "When should you do it?",
                    answ: "At your earliest convenience.",
                    class: 'panelHeaderClass'}
            ]
        }
    },
	mounted() {
        // Send the reference to the parent
        this.$emit('reference', 'faqs', this.$refs['faqs']);
	},
    methods: {
        panelHeaderClassForRow1(event) {
            if (event.class === 'panelHeaderClass') {
                for (let i = 0; i < this.rowOne.length; i++) {
                    if (this.rowOne[i].question === event.question) {
                        this.rowOne[i].class = 'panelClickedHeaderClass';
                    } else {
                        this.rowOne[i].class = 'panelHeaderClass';
                    }
                }
            } else {
                for (let i = 0; i < this.rowOne.length; i++) {
                    if (this.rowOne[i].question === event.question) {
                        this.rowOne[i].class = 'panelHeaderClass';
                    }
                }
            }
        },
        panelHeaderClassForRow2(event) {
            if (event.class === 'panelHeaderClass') {
                for (let i = 0; i < this.rowTwo.length; i++) {
                    if (this.rowTwo[i].question === event.question) {
                        this.rowTwo[i].class = 'panelClickedHeaderClass';
                    } else {
                        this.rowTwo[i].class = 'panelHeaderClass';
                    }
                }
            } else {
                for (let i = 0; i < this.rowTwo.length; i++) {
                    if (this.rowTwo[i].question === event.question) {
                        this.rowTwo[i].class = 'panelHeaderClass';
                    }
                }
            }
        },
        loadMoreQuestions() {
            if (this.loadPanelClass === 'customBackgroundOneClass') {
                // load data in the arrays
                this.rowOne.push(this.moreInfo[0]);
                this.rowTwo.push(this.moreInfo[1]);

                this.message = 'SHOW LESS'
                this.loadPanelClass = 'customBackgroundTwoClass'
            } else {
                // erase data from the arrays
                this.rowOne = this.rowOne.filter(row => row.question != this.moreInfo[0].question);
                this.rowTwo = this.rowTwo.filter(row => row.question != this.moreInfo[1].question);

                this.message = 'LOAD MORE'
                this.loadPanelClass = 'customBackgroundOneClass'
            }
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
/* @import '../styles/howTo.css'; */
@import url('https://fonts.googleapis.com/css2?family=Rubik:wght@500&display=swap');

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
/*** Text ***/
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
/*** Question Section ***/
.questionBox1Class {
    position: absolute;
    width: 550px;
    height: 812px;
    margin-top: 688px;

    border: none;
	background: none;
}
.questionBox2Class {
    position: absolute;
    width: 550px;
    height: 812px;
    margin-top: 688px;
    margin-left: 570px;

    border: none;
	background: none;
}
.gridClass {
    display: grid;
    row-gap: 10px;
}
.whiteSpaceClass {
    width: 550px;
    height: 50px;
    padding-bottom: 50px;
}
/*** Panel properties ***/
.noBackground {
    background: #FFFFFF;
    border-radius: 10px;
}
.panelHeaderClass {
    width: 550px;
    height: 90px;
    /* Box proprieties */
    background: #FFFFFF;
    box-shadow: 0px 20px 40px 0px rgba(238, 77, 71, 0.1);
    border-radius: 10px;
    background-image: url("../assets/faqs/Rectangle.png"), url("../assets/faqs/Rectangle2.png");
    background-repeat: no-repeat;
    background-position-x: 495px, 504px;
    background-position-y: 44px, 35px;
}
.panelClickedHeaderClass {
    width: 550px;
    height: 90px;
    /* Box proprieties */
    background: #FFFFFF;
    box-shadow: 0px 20px 40px 0px rgba(238, 77, 71, 0.1);
    border-radius: 10px;
    background-image: url("../assets/faqs/Rectangle.png");
    background-repeat: no-repeat;
    background-position-x: 495px;
    background-position-y: 44px;
}

.headerTextClass {
    position: absolute;
    width: 400px;
    height: 40px;
    font-family: Rubik;
    font-style: normal;
    font-weight: 500;
    font-size: 18px;
    line-height: 30px;
    display: flex;
    align-items: center;
    text-align: left;
    color: #402B2B;
}

.panelContentClass {
    width: 550px;
    height: 160px;
    /* Box proprieties */
    background: #FFF7F5;
    box-shadow: 0px 20px 40px rgba(238, 77, 71, 0.1);
    border-radius: 10px;
    /* text */
    font-family: Rubik;
    font-style: normal;
    font-weight: 300;
    font-size: 18px;
    line-height: 30px;
    display: flex;
    align-items: center;
    text-align: left;
    color: #402B2B;
}
/*** Load Panel ***/
.panelLoadClass {
    width: 550px;
    height: 90px;
    /* Box proprieties */
    background: #ED4D47;
    opacity: 0.3;
    border-radius: 10px;
}
.customBackgroundOneClass {
    margin-top: 10px;
    border-radius: 10px;
    border-top: none;

    background-image: url("../assets/faqs/Rectangle.png"), url("../assets/faqs/Rectangle2.png");
    background-repeat: no-repeat;
    background-position-x: 495px, 504px;
    background-position-y: 44px, 35px;
}
.customBackgroundTwoClass {
    margin-top: 13px;
    border-radius: 10px;
    border-top: none;

    background-image: url("../assets/faqs/Rectangle.png");
    background-repeat: no-repeat;
    background-position-x: 495px;
    background-position-y: 44px;
}

.loadPanelTextClass {
    position: absolute;
    width: 112px;
    height: 30px;
    margin-left: 219px;
    margin-top: 30px;
    font-family: Rubik;
    font-style: normal;
    font-weight: bold;
    font-size: 18px;
    line-height: 30px;
    display: flex;
    align-items: center;
    text-align: center;
    color: #ED4D47;
}

</style>
