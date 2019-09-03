<template>
  <div class="container quiz">
    <Navbar :text="message"></Navbar>
    <div v-for="(question, iQuestion) in questions" :key="iQuestion">
      <Question :question="question">
        <Options :started="started" v-for="(option, iOption) in options[iQuestion]" :key="iOption" :options="option" :answer="answers[iQuestion]" @start="start" @correct="changeScore"></Options>
      </Question>
    </div>
    <Result :started="started" :right="right">
      <button
        class="element-animation1 btn btn-lg btn-dark btn-block"
        v-on:click="reset"
        data-test="refazer"
      >
        Refazer o Quiz
      </button>
    </Result>
  </div>
</template>

<script>
import Navbar from "@/components/Navbar";
import Question from "@/components/Question";
import Options from "@/components/Options";
import Result from "@/components/Result";

export default {
  data: () => ({
    message:
      "Adivinhe os personagens do desenho Irmão do Jorel e concorra a prêmios!",
    questions: [
      {
        src:
          "https://abrilsuperinteressante.files.wordpress.com/2016/10/super_imgirmao_jorel.png",
        alt: "Personagem questao 1"
      },
      {
        src: "https://i.ytimg.com/vi/QXWINUsBUjk/maxresdefault.jpg",
        alt: "Personagem questao 2"
      },
      {
        src: "https://i.ytimg.com/vi/_0_Wifw9q1A/maxresdefault.jpg",
        alt: "Personagem questao 3"
      }
    ],
    options: [
      {
        option: ["Joel", "Joesley", "Jorel ", "Irmão do Jorel"]
      },
      {
        option: ["Vovó Juju", "Vovó Joana", "Vovó July ", "Vovó Jane"]
      },
      {
        option: [
          "Caro Felino",
          "Carlito Felino",
          "Carlos Felino",
          "Charles Felino"
        ]
      }
    ],
    answers: [3, 0, 2],
    right: 0,
    started: false
  }),
  methods: {
    changeScore() {
      this.right++
    },
    reset() {
      this.started = false;
      this.right = 0;
    },
    start() {
      this.started = true;
    }
  },
  components: {
    Navbar,
    Question,
    Options,
    Result
  }
};
</script>