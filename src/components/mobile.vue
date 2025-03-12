<script setup lang="js">
import { ref, onMounted, onUnmounted, computed } from "vue";
import Cards from "./card.vue";
import Forms2 from "./forms2.vue";
import TelaMobile1 from "./TelaMobile1.vue";
const oucaagoraApp = () => {
  window.location.href = "https://www.youtube.com/@redfoxtvoficial";
};
const TamanhoTela = ref(window.innerWidth);
const Mobile = computed(() => TamanhoTela.value <= 1021);
const Desktop = computed(() => TamanhoTela.value > 1021);
const AtualizarTamanhoTela = () => {
  TamanhoTela.value = window.innerWidth;
};
onMounted(() => {
  window.addEventListener("resize", AtualizarTamanhoTela);
});
onUnmounted(() => {
  window.removeEventListener("resize", AtualizarTamanhoTela);
});
const LeadsWhatsapp = () => {
  window.location.href = "https://api.whatsapp.com/send?phone=5511968713163";
}
</script>
<template>
  <div class="Modelos">
    <div v-show="Desktop" class="pc">
      <div class="container">
        <div class="contentBackground-ImageAdilson">
          <div class="logoNav">
            <img style="width: 300px" src="../imagesHome/1.svg" alt="" />
          </div>
          <div class="contentCopy">
            <div class="copy">
              <h1>
                <span style="color: #d40d35">Trajetórias</span> Reais, <br />
                Conquistas Incríveis – <br />
                Direto de
                <span style="color: #d40d35">Guarulhos</span>
              </h1>
              <button
                @click="oucaagoraApp"
                style="
                  border-radius: 10px;
                  width: 297px;
                  height: 60px;
                  background-color: #6e071c;
                  color: white;
                  font-size: 18px;
                  font-weight: bold;
                  border: none;
                  cursor: pointer;
                  box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.2);
                  transition: background-color 0.3s ease;
                "
                onmouseover="this.style.backgroundColor='#8a0a24'"
                onmouseout="this.style.backgroundColor='#6e071c'"
              >
                <i class="fas fa-headphones"></i>
                OUÇA AGORA
              </button>
            </div>
          </div>
        </div>
        <div class="BannerPropaganda"></div>
        <div class="SecaoDCards">
          <div class="tituloCards">
            <h1>
              <span style="color: #d40d35">Inspire-se </span>com Episódios que
              Estão <br />
              Fazendo a <span style="color: #d40d35">Diferença</span> !
            </h1>
          </div>
          <div class="LocalCards">
            <Cards />
          </div>
        </div>
        <div class="secaoPodcast">
          <div class="TittlePodcast">
            <h1>
              Para Quem é o Nosso <br />
              <span style="color: #d40d35">Podcast</span>?
            </h1>
            <br />
            <br />
            <div class="listaPodcast">
              <ul style="list-style-type: none; padding-left: 0">
                <li>
                  <i
                    class="fas fa-check"
                    style="color: red; margin-right: 8px"
                  ></i>
                  <span style="color: #fff; font-family: sans-serif">
                    Para aqueles que estão em busca de inspiração e aprendizado
                    <br />
                    com histórias de sucesso no mundo dos negócios.
                  </span>
                </li>
                <br />
                <li>
                  <i
                    class="fas fa-check"
                    style="color: red; margin-right: 8px"
                  ></i>
                  <span style="color: #fff; font-family: sans-serif">
                    Empreendedores que buscam novas perspectivas e <br />
                    estratégias para impulsionar seus projetos.
                  </span>
                </li>
                <br />
                <li>
                  <i
                    class="fas fa-check"
                    style="color: red; margin-right: 8px"
                  ></i>
                  <span style="color: #fff; font-family: sans-serif">
                    Aqueles que querem se conectar com mentes brilhantes de
                    <br />
                    diversos setores e aprender com suas trajetórias.
                  </span>
                </li>
                <br />
                <li>
                  <i
                    class="fas fa-check"
                    style="color: red; margin-right: 8px"
                  ></i>
                  <span style="color: #fff; font-family: sans-serif">
                    Profissionais que desejam entender como transformar <br />
                    desafios em oportunidades reais.
                  </span>
                </li>
              </ul>
              <div
                class="botaoAçao"
                style="display: flex; justify-content: center; width: 60%"
              >
                <button
                  @click="LeadsWhatsapp"
                  style="
                    border-radius: 10px;
                    width: 297px;
                    height: 60px;
                    background-color: #6e071c;
                    color: white;
                    font-size: 18px;
                    font-weight: bold;
                    border: none;
                    cursor: pointer;
                    box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.2);
                    transition: background-color 0.3s ease;
                  "
                  onmouseover="this.style.backgroundColor='#8a0a24'"
                  onmouseout="this.style.backgroundColor='#6e071c'"
                >
                  PARTICIPE DA CONVERSA
                </button>
              </div>
            </div>
          </div>
        </div>
        <div class="secaoFormulario">
          <div
            style="
              display: flex;
              flex-direction: column;
              text-align: center;
              padding-top: 50px;
            "
          >
            <h1 style="color: #fff; font-family: 'Poppins', sans-serif">
              Comece sua jornada de sucesso agora!
            </h1>
            <p style="color: #fff">
              Preencha o formulário para nos conhecermos
            </p>
          </div>
          <Forms2 />
          <p style="color: #fff; font-family: 'Poppins', sans-serif">
            @ 2025 Redfox
          </p>
        </div>
      </div>
    </div>
    <div v-show="Mobile" class="celular">
      <TelaMobile1 />
    </div>
  </div>
</template>
<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.Modelos {
  height: 100vh;
  width: 100%;
}
.pc {
  background-color: rgb(6, 88, 116);
  height: 100vh;
}
.contentBackground-ImageAdilson {
  height: 91vh;
  width: 100%;
  background-image: url(../imagesHome/5.svg);
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  display: flex;
  flex-direction: column;
  justify-content: right;
  align-items: right;
}
.logoNav {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 40%;
  width: 50%;
}
.contentCopy {
  display: flex;
  flex-direction: column;
  align-items: center;
  height: 30%;
  width: 57%;
  color: aliceblue;
}
.contentCopy h1 {
  font-family: sans-serif;
  font-size: 2.5rem;
}
.copy {
  gap: 25px;
}
.copy button {
  margin-top: 20px;
}
.BannerPropaganda {
  height: 20vh;
  width: 100%;
  background-image: url(../imagesHome/6.png);
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;

  display: flex;
  align-items: center;
  justify-content: center;
}
.SecaoDCards {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  height: 100vh;
  width: 100%;
  gap: 5rem;
  background-color: #131313;
}
.SecaoDCards h1 {
  font-family: sans-serif;
  font-size: 2.5rem;
  color: white;
}
.tituloCards {
  text-align: center;
}
.LocalCards {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 75%;
  height: 60%;
}
.secaoPodcast {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  height: 88vh;
  width: 100%;
  background-color: #2d2d2d;
}
.TittlePodcast h1 {
  font-family: "monserrat", sans-serif;
  font-size: 2.5rem;
  font-weight: bold !important;
  color: white;
}
.listaPodcast {
  display: flex;
  align-items: right;
  justify-content: right;
  width: 100%;
  flex-direction: column;
  gap: 5rem;
}
.listaPodcast li {
  text-decoration: none;
  color: white;
  font-size: 1.5rem;
  font-family: "monserrat", sans-serif;
  list-style-type: none;
  display: flex;
}
.secaoFormulario {
  width: 100%;
  height: 85vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background-color: #d40d35;
  gap: 1rem;
}
.celular {
  background-color: lightcoral;
}
@media screen and (min-width: 1030px) {
  .secaoFormulario {
    height: auto;
  }
}
</style>
