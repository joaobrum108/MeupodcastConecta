<script setup>
import Card from "./card.vue";
</script>
<template>
  <div class="telaMobile">
    <div class="sectionFirst">
      <div class="containerIformacao">
        <div class="conteudoGroup">
          <div><img src="../imagesHome/1.svg" alt="" /></div>
          <h2>
            <span style="color: #d40d35">Trajetórias</span> Reais, <br />
            Conquistas Incríveis – <br />
            Direto de <span style="color: #d40d35">Guarulhos</span>
          </h2>
          <div>
            <button
              style="
                border-radius: 10px;
                width: 70px;
                height: 20px;
                background-color: #6e071c;
                color: white;
                font-size: 0.3rem;
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
    </div>
    <div class="BannerConteudo"></div>
    <div class="CarroselCards">
      <div class="conteudoCentro">
        <h2 style="text-align: center">
          <span style="color: #d40d35">Inspire-se </span>com Episódios que Estão
          <br />
          Fazendo a <span style="color: #d40d35">Diferença</span> !
        </h2>
      </div>
      <div class="componenteCard">
        <Card />
      </div>
    </div>
    <div class="conteudoCast">
      <div class="containerPodcastConteudo">
        <h2>
          Para Quem é o Nosso <span style="color: #d40d35">Podcast</span>?
        </h2>
        <div class="questionarioConteudo">
          <ul style="list-style-type: none; padding-left: 0">
            <li>
              <i class="fas fa-check" style="color: red; margin-right: 8px"></i>
              <span style="color: #fff; font-family: sans-serif">
                Para aqueles que estão em busca de inspiração e aprendizado
                <br />
                com histórias de sucesso no mundo dos negócios.
              </span>
            </li>
            <br />
            <li>
              <i class="fas fa-check" style="color: red; margin-right: 8px"></i>
              <span style="color: #fff; font-family: sans-serif">
                Empreendedores que buscam novas perspectivas e <br />
                estratégias para impulsionar seus projetos.
              </span>
            </li>
            <br />
            <li>
              <i class="fas fa-check" style="color: red; margin-right: 8px"></i>
              <span style="color: #fff; font-family: sans-serif">
                Aqueles que querem se conectar com mentes brilhantes de
                <br />
                diversos setores e aprender com suas trajetórias.
              </span>
            </li>
            <br />
            <li>
              <i class="fas fa-check" style="color: red; margin-right: 8px"></i>
              <span style="color: #fff; font-family: sans-serif">
                Profissionais que desejam entender como transformar <br />
                desafios em oportunidades reais.
              </span>
            </li>
          </ul>
          <div
            class="botaoAçao"
            style="display: flex; justify-content: center; width: 60%c"
          >
            <button
              class="btn2"
              style="
                border-radius: 10px;
                width: 100px;
                height: 15px;
                text-align: center;
                background-color: #6e071c;
                color: white;
                font-size: 0.4rem;
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
    <div class="caixafinalFormulario">
      <div class="info-1">
        <h2 style="text-align: center">
          Comece sua jornada de <br />
          sucesso agora!
        </h2>
        <h4 style="color: #fff; font-size: 0.5rem">
          Preencha o formulário para nos conhecermos
        </h4>
        <button
          style="
            border-radius: 10px;
            width: 160px;
            height: 15px;
            text-align: center;
            background-color: #aa0a2a;
            color: white;
            font-size: 0.4rem;
            font-weight: bold;
            border: none;
            cursor: pointer;
            box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.2);
            transition: background-color 0.3s ease;
          "
          onmouseover="this.style.backgroundColor='#8a0a24'"
          onmouseout="this.style.backgroundColor='#6e071c'"
        >
          VENHA NOS CONTAR SUA HISTORIA
        </button>
      </div>
    </div>
  </div>
</template>
<style scoped>
@media (max-width: 200px) {
  .info-1 {
    display: flex;
    flex-direction: column;
    text-align: center;
    align-items: center;
    gap: 1rem;
    padding: 10px;
  }
  .caixafinalFormulario {
    background-color: #d40d35;
    display: flex;
    flex-direction: column;
    height: 20dvh;
  }
  .questionarioConteudo {
    height: 180px;
    width: 80%;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 1rem;
  }
  li {
    text-align: left;
    font-size: 0.6rem;
  }
  .containerPodcastConteudo {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center !important;
    height: 80%;
    gap: 1rem;
  }
  .conteudoCast {
    background-color: #2d2d2d;
    height: 50dvh;
  }
  .conteudoCentro {
    display: flex;
    flex-direction: column;
    justify-content: center;
    height: 50px;
  }
  .CarroselCards {
    background-color: #131313;
    height: auto;
    min-height: 200px !important;
  }
  .BannerConteudo {
    background-image: url(../imagesHome/6.PNG);
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    width: 100%;
    height: auto;
    min-height: 50px;
  }
  .conteudoGroup {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: auto;
    gap: 1rem;
  }
  .telaMobile {
    width: 100%;
    height: 100vh;
  }
  .sectionFirst {
    background-image: url(../imagesHome/5.svg);
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    width: 100%;
    height: 180px;
    display: flex;
    align-items: center;
  }
  img {
    width: 35%;
  }
  h2 {
    font-size: 0.6rem !important;
    color: #fff;
  }
}
@media (min-width: 201px) and (max-width: 600px) {
  .info-1 {
    display: flex;
    flex-direction: column;
    text-align: center;
    align-items: center;
    gap: 1rem;
    padding: 10px;
  }
  .caixafinalFormulario {
    background-color: #d40d35;
    display: flex;
    flex-direction: column;
    height: 20dvh;
  }
  .questionarioConteudo {
    height: 180px;
    width: 80%;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 1rem;
  }
  li {
    text-align: left;
    font-size: 0.9rem;
  }
  .containerPodcastConteudo {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center !important;
    height: 80%;
    gap: 1rem;
  }
  .conteudoCast {
    background-color: #2d2d2d;
    height: 88dvh;
  }

  .conteudoCentro {
    display: flex;
    flex-direction: column;
    justify-content: center;
    height: 50px;
  }
  .CarroselCards {
    background-color: #131313;
    height: auto;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    min-height: 260px !important;
  }
  .BannerConteudo {
    background-image: url(../imagesHome/6.PNG);
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    width: 100%;
    height: auto;
    min-height: 50px;
  }
  .conteudoGroup {
    display: flex;
    flex-direction: column;
    align-items: start !important;
    justify-content: left !important;
    width: 280px;
    gap: 1rem;
  }
  .telaMobile {
    width: 100%;
    height: 100vh;
  }
  .sectionFirst {
    background-image: url(../imagesHome/5.svg);
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    justify-content: center;
    width: 100%;
    height: 180px;
    display: flex;
    align-items: center;
  }
  img {
    width: 35%;
  }
  h2 {
    font-size: 0.9rem !important;
    color: #fff;
    font-family: "poppins", sans-serif;
  }
  .btn2 {
    font-size: 0.7rem !important;
    width: 160px !important;
    height: 35px !important;
  }
}

@media (min-width: 600px) and (max-width: 1021px) {
  .info-1 {
    display: flex;
    flex-direction: column;
    text-align: center;
    align-items: center;
    gap: 1rem;
    padding: 10px;
  }
  .caixafinalFormulario {
    background-color: #d40d35;
    display: flex;
    flex-direction: column;
    height: 35dvh !important;
  }
  .questionarioConteudo {
    height: 180px;
    width: 80%;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 1rem;
  }
  li {
    text-align: left;
    font-size: 0.8rem;
  }
  .containerPodcastConteudo {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center !important;
    height: 80%;
    gap: 1rem;
  }
  .conteudoCast {
    background-color: #2d2d2d;
    height: 95dvh;
  }

  .conteudoCentro {
    display: flex;
    flex-direction: column;
    justify-content: center;
    height: 50px;
  }
  .CarroselCards {
    background-color: #131313;
    height: auto;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    min-height: 260px !important;
  }
  .BannerConteudo {
    background-image: url(../imagesHome/6.PNG);
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    width: 100%;
    height: auto;
    min-height: 100px;
  }
  .conteudoGroup {
    display: flex;
    flex-direction: column;
    align-items: start !important;
    justify-content: left !important;
    width: 280px;
    gap: 1rem;
  }
  .telaMobile {
    width: 100%;
    height: 100vh;
  }
  .sectionFirst {
    background-image: url(../imagesHome/5.svg);
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    justify-content: center;
    width: 100%;
    height: 350px !important;
    display: flex;
    align-items: center;
  }
  img {
    width: 40%;
  }
  h2 {
    font-size: 1.5rem !important;
    color: #fff;
    font-family: "poppins", sans-serif;
  }
  .btn2 {
    font-size: 0.7rem !important;
    width: 160px !important;
    height: 35px !important;
  }
}
</style>
