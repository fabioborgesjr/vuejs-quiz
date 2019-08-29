<template>
  <div class="container quiz">
    <Navbar :text="message"></Navbar>
    <Question
      question="Qual personagem é esse?"
      src="https://abrilsuperinteressante.files.wordpress.com/2016/10/super_imgirmao_jorel.png"
      alt="https://abrilsuperinteressante.files.wordpress.com/2016/10/super_imgirmao_jorel.png"
    ></Question>
    <Options :options="options1"></Options>
    <Question
      question="Qual personagem é esse?"
      src="https://i.ytimg.com/vi/QXWINUsBUjk/maxresdefault.jpg"
      alt="https://i.ytimg.com/vi/QXWINUsBUjk/maxresdefault.jpg"
    ></Question>
    <Options :options="options2"></Options>
    <Question
      question="Qual personagem é esse?"
      src="https://i.ytimg.com/vi/_0_Wifw9q1A/maxresdefault.jpg"
      alt="https://i.ytimg.com/vi/_0_Wifw9q1A/maxresdefault.jpg"
    ></Question>
    <Options :options="options3"></Options>
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
    options1: ["Joel", "Joesley", "Jorel ", "Irmão do Jorel"],
    options2: ["Vovó Juju", "Vovó Joana", "Vovó July ", "Vovó Jane"],
    options3: ["Caro Felino", "Carlito Felino", "Carlos Felino ", "Charles Felino"]  
  }),
  components: {
    Navbar,
    Question,
    Options
  }
};
</script>