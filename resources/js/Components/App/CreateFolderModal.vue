<template>
   <modal :show="modelValue" max-width="sm">
        <div class="p-6">
            <h2 class="text-lg font-medium text-gray-900"> Create New Folder</h2>
            <div class="mt-6">
                <input-label for="folderName" value="folderName" class="sr-only"/>
                <text-input
                    ref="folderNameInput"
                    class="mt-1 block w-full"
                    :class="form.errors.name ? 'border-red-500 focus:border-red-500 focus:ring-red-500':'' "
                    type="text" id="folderName"
                    placeholder="Folder Name"
                    @keyup.enter="createFolder"
                />
                <input-error :message="form.errors.name" class="mt-2" />
            </div>
            <div class="mt-6 flex justify-end gap-3">
                <secondary-button @click="closeModal" > Cancel</secondary-button>
                <primary-button @click="createFolder" :class="{ 'opacity-25': form.processing }" :disabled="form.processing" > Submit</primary-button>
            </div>
        </div>
   </modal>

</template>
<script setup>

import Modal from "@/Components/Modal.vue";
import InputLabel from "@/Components/InputLabel.vue";
import TextInput from "@/Components/TextInput.vue";
import InputError from "@/Components/InputError.vue";
import {useForm} from "@inertiajs/vue3";
import SecondaryButton from "@/Components/SecondaryButton.vue";
import PrimaryButton from "@/Components/PrimaryButton.vue";
import {ref} from "vue";
const folderNameInput=ref(null)
const {modelValue}=defineProps({
    modelValue:Boolean
})
const emit=defineEmits(['update:modelValue'])
const form=useForm({
    name:``
})
const closeModal=()=>{
    emit('update:modelValue')
    form.clearErrors()
    form.reset()
}
const createFolder=()=>{
    console.log('create folder')
    form.post(route('folder.create'),{
        preserveScroll:true,
        onSuccess:()=>{
            closeModal()
            form.reset()
        },
        onError:()=>  folderNameInput.value.focus()
    })
}
</script>
