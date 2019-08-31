<template>
  <div class="container quiz">
    <Navbar :text="message"></Navbar>
    <Question
      question="Qual personagem é esse?"
      src="https://abrilsuperinteressante.files.wordpress.com/2016/10/super_imgirmao_jorel.png"
      alt="https://abrilsuperinteressante.files.wordpress.com/2016/10/super_imgirmao_jorel.png"
    >
      <Options
        :options="options1"
        :answer="answers.q1"
        @correct="right++"
      ></Options>
    </Question>
    <Question
      question="Qual personagem é esse?"
      src="https://i.ytimg.com/vi/QXWINUsBUjk/maxresdefault.jpg"
      alt="https://i.ytimg.com/vi/QXWINUsBUjk/maxresdefault.jpg"
    >
      <Options
        :options="options2"
        :answer="answers.q2"
        @correct="right++"
      ></Options>
    </Question>
    <Question
      question="Qual personagem é esse?"
      src="https://i.ytimg.com/vi/_0_Wifw9q1A/maxresdefault.jpg"
      alt="https://i.ytimg.com/vi/_0_Wifw9q1A/maxresdefault.jpg"
    >
      <Options
        :options="options3"
        :answer="answers.q3"
        @correct="right++"
      ></Options>
    </Question>
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
    options1: ["Joel", "Joesley", "Jorel ", "Irmão do Jorel"],
    options2: ["Vovó Juju", "Vovó Joana", "Vovó July ", "Vovó Jane"],
    options3: [
      "Caro Felino",
      "Carlito Felino",
      "Carlos Felino",
      "Charles Felino"
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