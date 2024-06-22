<template>
    <nav class="min-w-[200px]">
        <div class="h-[80px] flex items-center gap-3">
            <Link href="/">
                <ApplicationLogo class="block h-9 w-auto fill-current text-gray-800"/>
            </Link>
            Lara Storage
        </div>
    </nav>
</template>
<script setup>
import {Link} from "@inertiajs/vue3";
import ApplicationLogo from "@/Components/ApplicationLogo.vue";
</script>
