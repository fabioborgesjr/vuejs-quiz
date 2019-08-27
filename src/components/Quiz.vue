<template>
  <div class="container">
    <Navbar :text="message"></Navbar>
    <Question
      question="Qual personagem é esse?"
      src="https://abrilsuperinteressante.files.wordpress.com/2016/10/super_imgirmao_jorel.png"
      alt="https://abrilsuperinteressante.files.wordpress.com/2016/10/super_imgirmao_jorel.png"
    ></Question>
    <Options :options="options1"></Options>
  </div>
</template>

<script>
import Navbar from "@/components/Navbar";
import Question from "@/components/Question";
import Options from "@/components/Options";

export default {
  data: () => ({
    message:
      "Adivinhe os personagens do desenho Irmão do Jorel e concorra a prêmios!",
    options1: ["Cleiton", "Joesley", "Jorel ", "Irmão do Jorel"]
  }),
  components: {
    Navbar,
    Question,
    Options
  }
};
</script>