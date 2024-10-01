<template>
    <Menu as="div" class="relative block text-left">
        <!-- MenuButton toggles the dropdown visibility -->
        <MenuButton
            class="flex w-full justify-center rounded-md gap-x-1.5 px-3 py-2 text-sm shadow-sm font-medium text-gray-900 ring-1 ring-inset ring-gray-300 hover:bg-gray-100"
        >
            Create New
        </MenuButton>

        <!-- Transition for smooth dropdown display -->
        <transition
            enter-active-class="transition duration-100 ease-out"
            enter-from-class="transform scale-95 opacity-0"
            enter-to-class="transform scale-100 opacity-100"
            leave-active-class="transition duration-75 ease-in"
            leave-from-class="transform scale-100 opacity-100"
            leave-to-class="transform scale-95 opacity-0"
        >
            <!-- MenuItems for dropdown options -->
            <MenuItems
                class="absolute md:left-0 bottom-full mb-2 md:top-full md:mt-2 w-40 origin-bottom-right md:origin-top-right divide-y divide-gray-100 rounded-md shadow-lg ring-1 ring-black/5 focus:outline-none"
            >
                <div class="px-5 py-1 bg-white  hover:bg-gray-50 ">
                    <MenuItem>
                        <a class="block text-gray-800 font-semibold px-2 py-3 text-sm cursor-pointer">
                            New Folder
                        </a>
                    </MenuItem>
                </div>
                <div class="px-5 py-1 bg-white  hover:bg-gray-50">
                    <MenuItem>
                        <a class="block text-gray-800 font-semibold px-2 py-3 text-sm cursor-pointer">
                            New File
                        </a>
                    </MenuItem>
                </div>
                <div class="px-5 py-1 bg-white  hover:bg-gray-50">
                    <MenuItem>
                        <a class="block text-gray-800 font-semibold  px-2 py-3 text-sm cursor-pointer">
                            New Upload
                        </a>
                    </MenuItem>
                </div>
            </MenuItems>
        </transition>
    </Menu>
</template>

<script setup>
import { Menu, MenuButton, MenuItem, MenuItems } from "@headlessui/vue";
</script>
