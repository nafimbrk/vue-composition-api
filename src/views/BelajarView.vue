<script setup>
import { ref, reactive, computed } from "vue"

const message = ref('hello <strong>world</strong>')
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

const handsome = true

const nilai = 'A'

const fruits = ['apple', 'mango', 'banana', 'melon', 'orange']

const students = [
    { name: 'Ben', age: 9 },
    { name: 'Jack', age: 10 },
    { name: 'Ted', age: 11 }
]

const hiYou = () => alert('halo kamu')

const checkUsername = () => alert('kamu belum input username')

const onEnter = () => alert('test keyup')

const pikachuUrl = 'data:image/jpeg;base64,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'

const fontSize = 50

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

    <hr style="margin: 20px 0px;">

    <div v-text="message"></div>
    <div v-html="message"></div>

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
    <div v-else>nilai kamu tidak ada di predikat</div>

    <hr>

    <div v-for="item in fruits">
        {{ item }}
    </div>

    <div v-for="(fruit, index) in fruits" :key="index">
        {{ `${index + 1}. ${fruit}` }}
    </div>

    <div v-for="student in students">
        {{ `${student.name} (${student.age})` }}
    </div>

    <hr>

    <button @click="hiYou">click me</button>

    <form action="https://google.com" @submit.prevent="checkUsername">
        <input type="text" name="" id="">
        <input type="submit">
    </form>

    <br>

    <input type="text" name="" id="" @keyup.enter="onEnter">

    <img :src="pikachuUrl" alt="">

    <div :style="{ fontSize: fontSize + 'px'}">ini test font size</div>

    <hr>
    <input type="text" name="" id="" v-model="number">
    <hr>
</template>

<style scoped></style>