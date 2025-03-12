<template>
  <div class="form-container">
    <form @submit.prevent="submitForm">
      <div class="form-group">
        <label for="celular">Celular:</label>
        <input type="text" id="celular" v-model="form.celular" required />
      </div>

      <div class="form-group">
        <label for="email">E-mail:</label>
        <input type="email" id="email" v-model="form.email" required />
      </div>

      <div class="form-group">
        <label for="profissao">Profissão:</label>
        <input type="text" id="profissao" v-model="form.profissao" required />
      </div>

      <div class="form-group">
        <label for="mensagem">Mensagem (opcional):</label>
        <textarea id="mensagem" v-model="form.mensagem"></textarea>
      </div>

      <div class="form-group">
        <button type="submit">Enviar</button>
      </div>
    </form>
  </div>
</template>

<script setup>
import { ref } from "vue";

const form = ref({
  celular: "",
  email: "",
  profissao: "",
  mensagem: "",
});

const submitForm = () => {
  console.log("Formulário enviado:", form.value);

  form.value = {
    celular: "",
    email: "",
    profissao: "",
    mensagem: "",
  };
};
</script>
<style scoped>
.form-container {
  width: 25% !important;
  height: 500px !important;
  padding: 20px;
  border: 1px solid #ccc;
  background: rgba(255, 255, 255, 0.1);
  border-radius: 10px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
}

.form-group {
  margin-bottom: 20px;
}

label {
  display: block;
  margin-bottom: 8px;
  color: #ffffff;
  font-size: 0.9rem;
}

input,
textarea {
  width: 100%;
  padding: 10px;
  box-sizing: border-box;
  background: rgba(255, 255, 255, 0.1);
  border: 1px solid rgba(255, 255, 255, 0.3);
  border-radius: 5px;
  color: #ffffff;
  font-size: 0.9rem;
}

textarea {
  resize: vertical;
  min-height: 100px;
}

button {
  width: 100%;
  padding: 12px;
  background-color: #970926;
  color: white;
  border: none;
  border-radius: 5px;
  font-size: 1rem;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

button:hover {
  background-color: #7a0720;
}

@media screen and (min-width: 1030px) {
  .form-container {
    width: 550px !important;
    height: 500px !important;
    padding: 30px;
  }

  button {
    width: auto;
    padding: 12px 30px;
  }
}
</style>
