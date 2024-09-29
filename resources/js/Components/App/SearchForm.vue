<script setup>
import TextInput from "@/Components/TextInput.vue";
import {useForm} from "@inertiajs/vue3";
const form=useForm({
    search:''
})
</script>

<template>
    <form class="w-[40vw] h-[80px] flex items-center  " action="">
        <TextInput type="text" class="w-full mr-2" v-model="form.search" placeholder="Search for file and folder"></TextInput>
    </form>
</template>
