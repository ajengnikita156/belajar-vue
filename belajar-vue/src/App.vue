<script setup>
let msg = "Hallo Kamu";
let headName = "<h1>NAMA SAYA AJENG<h1>";
let number = 4 ;
let ok = 'YES';
let seen = 1 ;
</script>

<template>
  <div>
    <span>{{ msg }}</span><br>
    <span style="color: yellowgreen;"> "warna yellowgreen" </span><br>
    <span v-html = "headName"></span>

    <div v-bind:id="dynamicId"></div>
    <button v-bind:disabled="isButtonDisabled">Tombol</button>
  <!-- ekspresi -->
    {{ number + 1 }} <br>
     {{ ok ? 'YES' : 'NO' }}
      {{ msg.split('').reverse().join('')
}}
    <div v-bind:id="'list-' + id"></div>

    <!-- direktri -->
    <p v-if="seen">Sekarang Anda bisa melihatku</p>

    <!-- argumen -->
    <a v-bind:href="url">siapa kamu </a><br>
    <a v-on:click="doSomething"> ?? </a><br>

    <!-- argumen dinamis -->
    <a v-bind:[namaAtribut]="url"> mau coba? </a><br>
    <a v-on:[namaEvent]="doSomething"> mau? </a><br>

    <!-- Modifier -->
    <form v-on:submit.prevent="onSubmit">LOGIN</form>

    <!-- Singkatan v-bind -->
    <!-- full syntax -->
    <a v-bind:href="url"> aku </a>

    <!-- singkatan -->
    <a :href="url"> AJENG </a>

    <!-- singkatan dengan argumen dinamis (2.6.0+) -->
    <a :[key]="url"> NIKITA </a><br>

    <!-- singkatan v-on -->
    <!-- full syntax -->
    <a v-on:click="doSomething"> ajeng </a>

    <!-- singkatan -->
    <a @click="doSomething"> nikita </a>

    <!-- singkatan argumen dinamis (2.6.0+) -->
    <a @[event]="doSomething"> anggraeni </a>
    <br><br>

    <select v-model="selected" multiple>
  <option>A</option>
  <option>B</option>
  <option>C</option>
</select>
<br>
<span>Yang dipilih: {{ selected }}</span>

<br><br>
<span>Masukan pesan anda:</span>
<p style="white-space: pre-line;">{{ pesan }}</p>
<br>
<textarea v-model="pesan" placeholder="Tambahkan pesan"></textarea>
<br>
<div v-bind:id="dynamicId"></div>
    <button v-bind:disabled="isButtonDisabled">Tombol</button>

  </div>
</template>