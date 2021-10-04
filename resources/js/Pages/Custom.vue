<template>
    <app-layout>
        <Head>
            <title>Your page title</title>
            <meta name="description" content="Your page description" />
        </Head>

        <template #header>
            <h2 class="font-semibold text-xl text-gray-800 leading-tight">
                Custom Test
            </h2>
        </template>

        <div class="py-12">
            <div class="max-w-7xl mx-auto sm:px-6 lg:px-8">
                <div class="bg-white overflow-hidden shadow-xl sm:rounded-lg">
                    <div class="h-56 flex flex-col justify-center items-center">
                        <h1 class="text-4xl font-bold mb-2">Holla Custom!</h1>
                        <Link
                            :href="route('dashboard')"
                            as="button"
                            :class="buttonStyles"
                        >
                            To Dashboard
                        </Link>
                    </div>
                </div>
            </div>
        </div>
    </app-layout>
</template>

<script>
import { defineComponent } from "vue";
import { Link, Head } from "@inertiajs/inertia-vue3";
import AppLayout from "@/Layouts/AppLayout.vue";

export default defineComponent({
    components: {
        Link,
        Head,
        AppLayout,
    },

    computed: {
        buttonStyles() {
            return `border border-gray-400 hover:border-purple-400 hover:text-purple-800 rounded px-4 py-2`;
        },
    },
});
</script>
