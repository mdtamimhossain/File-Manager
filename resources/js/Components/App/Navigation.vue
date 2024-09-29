<template>
    <nav class="min-w-[200px] hidden md:block">
        <div class="px-3 flex md:block">
            <create-new-dropdown  />
            <div class="py-3 flex flex-row md:flex-col">
                <NavLink href="/">My Files</NavLink>
                <NavLink href="/">Shared With me</NavLink>
                <NavLink href="/">Shared by me</NavLink>
                <NavLink href="/">Trash</NavLink>
            </div>
        </div>
    </nav>
</template>

<script setup>
import CreateNewDropdown from "@/Components/App/CreateNewDropdown.vue";
import NavLink from "@/Components/NavLink.vue";
</script>
