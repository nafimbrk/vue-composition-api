<script setup>
import { ref, reactive } from "vue"

const message = ref('hello world')
const number = ref(0)
const student = reactive({
    name: 'jack',
    age: 9
})

// reactive gk bisa digunakan untuk tipe data yg primitive (string, boolean, number) bisanya untuk tipe data (object, array, collection)

console.log(message.value)

console.log(student.name)

</script>

<template>
    <h1>ini halaman belajar view</h1>
    {{ message }}
    <br>
    {{ number }}
    <br>
    {{ student.name }}
    <br>
    <ul v-for="item in student">
        <li>{{ item }}</li>
    </ul>
</template>

<style scoped></style>