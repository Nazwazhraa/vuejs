<script setup>

import {ref} from 'vue';

     let msg = "Hai,";
     let headName = "<h2>Kamu terlihat seperti pencuri</h2>"
     let number = 7;
     let ok = "YES";
     let seen = true; //1 atau 2

// split reverse massage 
let massage = ref("hai Vue JS");
function balikkanPesan() {
  massage.value = massage.value.split('').reverse('').join('');
} 

// pengulangan 
let todos = [
{ teks: 'Belajar JavaScript' },
{ teks: 'Belajar Vue '},
{ teks: 'Buat Proyek Keren'}
]

// input
let pesan = ref("Hai Vue");
</script>
<template> 
    <div>
       <span>{{ msg }}</span><br>
       <span style="color:goldenrod">Bung.</span><br>
       <span v-html="headName"></span>
    </div>
    <div v-bind:id="dynamicId"></div> 
    <button v-bind:disabled="isButtonDisabled">Hasil pencurian kamu</button>
    {{ number + 1 }} <br>
    {{ ok ? 'YES' : 'NO' }} <br>
    {{ msg.split('').reverse().join('')}} <br>
    <p v-if="seen">Sekarang Anda bisa melihatku</p> 
  
  <!-- Split button -->
  <p>{{ massage }}</p>
  <button v-on:click="balikkanPesan">Balikan Pesan</button>

  <!-- for -->
  <br> pengulangan
  <ol>
    <li v-for="todo in todos">
    {{ todo.teks }}
  </li>
  </ol>

  <!-- input -->
  <p>{{ pesan }}</p>
  <input v-model="pesan">
  
<div v-bind:id="'list-' + id"></div> 

    <a v-bind:href="url"> Malah dipencet </a> <br>

    <a v-on:click="doSomething"> GG </a><br>

    <a v-bind:[namaAtribut]="url"> Beliin seblak </a><br>

    <a v-on:[namaEvent]="doSomething"> PELIT </a><br>

    <form v-on:submit.prevent="onSubmit">Yaudah</form><br>

    <!-- full syntax -->
<a v-bind:href="url"> Pundungan</a><br>

<!-- singkatan -->
<a :href="url"> Beli sendiri </a><br>

<!-- singkatan dengan argumen dinamis (2.6.0+) -->
<a :[key]="url"> oke </a><br>

<!-- full syntax -->
<a v-on:click="doSomething"> YAYAYAYA </a><br>

<!-- singkatan -->
<a @click="doSomething"> mksh </a><br>

<!-- singkatan argumen dinamis (2.6.0+) -->
<a @[event]="doSomething"> smsm </a><br>


    
</template> 
