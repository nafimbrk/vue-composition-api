<script setup>
import { ref, reactive, computed } from "vue";


        //  ini namanya state
        const message = ref('hello <b>world</b>')
        const number = ref(0)
        
        // selain ref ada reactive
        // untuk reactive gk bisa digunakan untuk tipe data yg primitif(string, boolean, number)
        // penggunaan nya untuk tipe data object, array, collection
        // const student = reactive({
        //     name: 'Eko',
        //     age: 20,
        //     level: 4
        // })
        // const student = reactive([
        //     'apple', 'orange', 'watermelon'
        // ])

        // ngambil value ref
        // console.log(message.value)

        // ngambil value reactive
        // console.log(student.name)


        const mentor = reactive({
            name: 'cara fajar',
            tutorials: [
                'html',
                'css',
                'js',
                'php',
                'vue',
                'laravel'
            ]
        })



        const hasTutorials = computed(() => mentor.tutorials.length > 0 ? 'ya' : 'no')


        const addNumber = () => number.value++


        const handsome = true


        const nilai = 'A'


        const fruits = [
            'apple', 'watermelon', 'banana'
        ]



        const students = [
            {name: 'Eko', age: 20},
            {name: 'Herman', age: 35}
        ]



        const hi = () => alert('halo')



        const checkUsername = () => alert('belum input username')



        const onEnter = () => alert('telah di enter')


        const gambarUrl = 'data:image/jpeg;base64,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'


        const fontSize = 50

</script>

<!-- minimal harus ada tag template biar gk error -->
<template>
<h1>ini halaman belajar vue</h1>
{{ message }}
<br>
<h3 style="margin-bottom: 0px;">{{ `current number is : ${number}` }}</h3>
<button @click="addNumber()" style="margin-bottom: 20px;">add number</button>
<!-- <br> -->
<!-- {{ student.name }} -->
<!-- {{ student[0] }} -->
  <!-- <ul v-for="item in student">
    <li>{{ item }}</li>
  </ul> -->

  <div style="border: solid 1px; background-color: #ddd; padding: 20px;">
    <p>{{ `nama mentor : ${mentor.name}` }}</p>
    <p>apakah punya tutorial ? {{ hasTutorials }}</p>
</div>

<hr style="margin: 20px 0px;">

<!-- <div v-text="message"></div> -->
<!-- v-text directive bisa juga ngebaca computed gk cuma state doang -->
<div v-text="hasTutorials"></div>

<!-- kalo udah pakai v-text atau v-html gk bisa ngetik apa" lagi di dalam tagnya -->
<!-- kalo v-html dia akan berubah jadi bold tapi kalo v-text tag <b></b> nya akan di print -->
<div v-html="message">
</div>

<div v-show="handsome">
    wah kamu tampan
</div>
<div v-if="handsome">
    wah kamu tampan
</div>

<hr>

<div v-if="nilai == 'B'">nilai kamu B</div>
<div v-else-if="nilai == 'A'">nilai kamu A</div>
<div v-else-if="nilai == 'C'">nilai kamu C</div>
<div v-else>nilai kamu tidak ada di prediksi</div>

<hr>

<div v-for="fruit in fruits">
    {{ fruit }}
</div>

<div v-for="(fruit, index) in fruits" :key="index">
    {{ `${index+1}. ${fruit}` }}
</div>

<div v-for="student in students">
    {{ `${student.name} (${student.name})` }}
</div>

<hr>

<button @click="hi">click me</button>

<form @submit.prevent="checkUsername" action="https://google.com">
    <input type="text">
    <input type="submit">
</form>

<br>

<input type="text" @keyup.enter="onEnter">


<img :src="gambarUrl" alt="">


<div :style="{ fontSize: fontSize + 'px' }">kashdsalk</div>

<hr>

<input type="text" v-model="number" />

</template>





<style scoped>
    
</style>