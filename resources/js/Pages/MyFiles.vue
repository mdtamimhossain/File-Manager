<template>
    <authenticated-layout>
        {{$page.url}}
    </authenticated-layout>
</template>
<script>

import {defineComponent} from "vue";
import AuthenticatedLayout from "@/Layouts/AuthenticatedLayout.vue";

export default defineComponent({
    components: {AuthenticatedLayout}
})
</script>
