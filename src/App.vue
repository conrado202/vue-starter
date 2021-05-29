<template>
  <div>
    <!-- CZESC 1 -->
    <!--<h1>Twoj email to: {{ email }}</h1>
    <h1>Sprawdzanie adresu email</h1>
    <h2>Twoj email to: {{ email }}</h2>

    <div v-if="email.length < 10">Ale masz krótki adres!</div>
    <div v-else-if="email.length < 15">Twój adres e-mail jest w sam raz.</div>
    <div v-else>Twój adres e-mail jest stanowczo za długi.</div> -->

    <!-- BINDING, reaktywnosc - Aplikacja reaktywnie zmienia stan komponentu i we wszystkich miejscach gdzie ten komponent zostal uzyty, ta zmiana sie aktualizuje -->
    <!-- jak robimy odwolnie do v-modelu, to jesli cos zmieniamy w oknie do wypisywania ro wniez sie to zmienia w naszym tekscie wyjsciowym  -->
    <!--<input type= "email" v-model="email">  
    <button @click="alertMyEmail()">Wyświetl mój e-mail w alercie</button> -->

    <!-- CZESC 2 -->
    <h1>Witaj w systemie do zapisow na zajecia</h1>
      <div v-if="authenticated">
         <h3>Jestes zalogowany jako: {{email}}</h3>
         <button @click="logOut()">Wyloguj sie</button>
      </div>

      <div v-else>
         Zaloguj sie:
              <input type= "text" v-model="email">  
              <button @click="logIn()">Zaloguj sie</button>
      </div>

  </div>


</template>

<script>


export default {
// CZESC 1
  // data() {
  //   return {
  //     email: 'bukowicz@student.agh.edu.pl',
  //     password: ''
  //   };
  // },

  // methods: {
  // alertMyEmail() {
  //   alert(this.email);
  //   }
  // }

// CZESC 2
  data() {
    return {
      authenticated: false
    };
  },

  methods: {
    logIn() {
      this.authenticated = true;
    },
    logOut() {
      this.authenticated = false;
      this.email = '';
    }
  }

}
</script>

<script>
  import "milligram";

  export default {
    // ...
  };
</script>

<style>

  /* Wszystkie znaczniki z odnosniekiem "button" maja miec zadany kolor */
button {
  background: blue;
  color: white;
}

</style>
