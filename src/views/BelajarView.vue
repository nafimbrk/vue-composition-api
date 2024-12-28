<script setup>
import { ref, reactive, computed } from "vue"

const message = ref('hello world')
const number = ref(0)
// const student = reactive({
//     name: 'jack',
//     age: 9
// })

// reactive gk bisa digunakan untuk tipe data yg primitive (string, boolean, number) bisanya untuk tipe data (object, array, collection)

// console.log(message.value)

// console.log(student.name)

const mentor = reactive({
    name: 'Cara Fajar',
    tutorials: [
        'Tutorial Html',
        'Tutorial Css',
        'Tutorial Javascript',
        'Tutorial Php',
        'Tutorial Laravel',
        'Tutorial Vue'
    ]
})

// const hasTutorials = computed(function () {
//     return mentor.tutorials.length > 0 ? 'Ya' : 'Tidak'
// })
const hasTutorials = computed(() => mentor.tutorials.length > 0 ? 'Ya' : 'Tidak')

// function addNumber() {
//     number.value++
// }
const addNumber = () => number.value++

</script>

<template>
    <h1>ini halaman belajar view</h1>
    {{ message }}
    <br>
    <h3 style="margin-bottom: 0px;">{{ `Current Number is: ${number}` }}</h3>
    <button @click="addNumber()" style="margin-bottom: 20px;">Add Number</button>
    <!-- <br>
    {{ student.name }}
    <br>
    <ul v-for="item in student">
        <li>{{ item }}</li>
    </ul> -->

    <div style="border: solid 1px; background-color: #ddd; padding: 20px;">
        <p>{{ `Nama Mentor: ${mentor.name}` }}</p>
        <!-- <p>Apakah Punya Tutorial ? {{ mentor.tutorials.length > 0 ? 'Ya' : 'Tidak' }}</p> -->
        <p>Apakah Punya Tutorial ? {{ hasTutorials }}</p>
    </div>
</template>

<style scoped></style>