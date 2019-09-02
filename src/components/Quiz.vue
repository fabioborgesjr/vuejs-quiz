<template>
  <div class="container quiz">
    <Navbar :text="message"></Navbar>
    <div v-for="(question, iQuestion) in questions" :key="iQuestion">
      <Question :question="question">
        <Options v-for="(option, iOption) in options[iQuestion]" :key="iOption" :options="option" :answer="answers.q1" @correct="right++"></Options>
      </Question>
    </div>
    <Result :right="right"></Result>
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
    answers: {
      q1: 3,
      q2: 0,
      q3: 2
    },
    right: 0
  }),
  components: {
    Navbar,
    Question,
    Options,
    Result
  }
};
</script>