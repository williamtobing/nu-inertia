<template>
    <Head>
        <title>Home</title>
    </Head>

    <section>
        <div class="py-8">
            <div class="max-w-7xl mx-auto sm:px-6 lg:px-8">
                <div
                    class="bg-gray-100 overflow-hidden shadow-xl sm:rounded-lg"
                >
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
    </section>
</template>

<script>
import { defineComponent } from "vue";
import { Link, Head } from "@inertiajs/inertia-vue3";

export default defineComponent({
    components: {
        Link,
        Head,
    },

    computed: {
        buttonStyles() {
            return `border border-gray-400 hover:border-purple-400 hover:text-purple-800 rounded px-4 py-2`;
        },
    },
});
</script>
