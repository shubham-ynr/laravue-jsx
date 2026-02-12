<script setup>
import { route } from "ziggy-js";
import { useAppearance } from "../composables/useAppearance";
import Button from "@/components/ui/button/Button.vue";

const { updateAppearance, resolvedAppearance } = useAppearance();

const handleApperance = () => {
    updateAppearance(resolvedAppearance.value === "dark" ? "light" : "dark");
};
</script>
<template>
    <div
        class="h-svh w-svw flex items-center justify-center flex-col bg-background text-foreground transition-colors duration-300"
    >
        <h1 class="text-2xl font-bold">Welcome to the Laravel Inertia</h1>

        <p>This is a simple welcome page</p>

        <Button variant="outline" class="mt-4" @click="handleApperance">
            Toggle Appearance: {{ resolvedAppearance }}
        </Button>

        <div class="text-center block mt-5">
            <p class="text-md">Page url: {{ route("welcome") }}</p>
            <p class="text-xs">Route url rendered from Ziggy</p>
        </div>
    </div>
</template>
