<template>
    <nav class="min-w-[200px]">

        <div class="px-3 flex md:hidden">
            <create-new-dropdown class="relative"/>
            <div class="flex justify-between w-full bg-gray-50 rounded-md px-5">
                <a class="flex items-center py-2 mr-1 px-5 border rounded-lg text-sm font-medium bg-gray-100" href="/" >Files</a>
                <a class="flex items-center py-2 mr-1 px-5 border rounded-lg text-sm font-medium bg-gray-100" href="/">Share</a>
                <a class="flex items-center py-2 mr-1 px-5 border rounded-lg text-sm font-medium bg-gray-100" href="/">Shared</a>
                <a class="flex items-center py-2 mr-1 px-5 border rounded-lg text-sm font-medium bg-gray-100" href="/">Trash</a>
            </div>
        </div>

    </nav>
</template>
<script setup>
import {Link} from "@inertiajs/vue3";
import ApplicationLogo from "@/Components/ApplicationLogo.vue";
import CreateNewDropdown from "@/Components/App/CreateNewDropdown.vue";
import NavLink from "@/Components/NavLink.vue";
import MobileNavLink from "@/Components/App/MobileNavLink.vue";
</script>
