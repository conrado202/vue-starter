<template>
  <div>
    <!-- <h1>Twoj email to: {{ email }}</h1> -->
    <h1>Sprawdzanie adresu email</h1>
    <h2>Twoj email to: {{ email }}</h2>

    <div v-if="email.length < 10">Ale masz krótki adres!</div>
    <div v-else-if="email.length < 15">Twój adres e-mail jest w sam raz.</div>
    <div v-else>Twój adres e-mail jest stanowczo za długi.</div>

      <!-- BINDING, reaktywnosc - Aplikacja reaktywnie zmienia stan komponentu i we wszystkich miejscach gdzie ten komponent zostal uzyty, ta zmiana sie aktualizuje -->
    <input type= "email" v-model="email">  <!-- jak robimy odwolnie do v-modelu, to jesli cos zmieniamy w oknie do wypisywania ro wniez sie to zmienia w naszym tekscie wyjsciowym  -->
    <button @click="alertMyEmail()">Wyświetl mój e-mail w alercie</button>
  
  </div>


</template>

<script>


export default {
  data() {
    return {
      email: 'bukowicz@student.agh.edu.pl',
      password: ''
    };
  },

  methods: {
  alertMyEmail() {
    alert(this.email);
    }
  }
}
</script>

<style>


</style>
