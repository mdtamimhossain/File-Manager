<script setup>
import { ref } from 'vue';
import { Link } from '@inertiajs/vue3';
import Navigation from "@/Components/App/Navigation.vue";
import SearchForm from "@/Components/App/SearchForm.vue";
import UserSettingsDropdown from "@/Components/App/UserSettingsDropdown.vue";
import ApplicationLogo from "@/Components/ApplicationLogo.vue";
import MobileNav from "@/Components/App/MobileNav.vue";

const showingNavigationDropdown = ref(false);
</script>

<template>

  <div class="h-screen bg-gray-50 w-full md:gap-4">
     <div class="flex flex justify-between items-center pr-2 lg:pr-0">
         <div class="h-[80px] flex items-center gap-3 px-4">
             <Link href="/">
                 <ApplicationLogo class="block h-9 w-auto fill-current text-gray-800"/>
             </Link>
             Personal Storage
         </div>
         <div class="hidden lg:flex">
             <SearchForm/>
         </div>
             <UserSettingsDropdown/>
     </div>
    <div>
        <main class="flex flex-col md:flex-row flex-1 px-4 overflow-hidden mt-5 md:mt-0">
            <div class="hidden md:flex">
                <Navigation/>
            </div>

            <div class="flex-1 flex flex-col overflow-hidden">
                <slot/>
            </div>
            <div class="fixed bottom-0 left-0 w-full lg:hidden mb-2">
                <MobileNav/>
            </div>
        </main>
    </div>
  </div>
</template>
