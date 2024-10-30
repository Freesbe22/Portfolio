<script>
export default {
    name: "navbar",
    data() {
        return {
            showMenu: false,
            selected: 0,
            hasScroll: false
        }
    },
    destroyed() {
        window.removeEventListener('scroll', this.actionScroll);
    }, created() {
        window.addEventListener('scroll', this.actionScroll);
        this.actionScroll();
    },
    methods: {
        toggleNavbar: function () {
            this.showMenu = !this.showMenu;
        },
        changeSelected: function (i) {
            this.selected = i;
        },
        actionScroll: function () {
            this.hasScroll = (window.scrollY === 0);
        }
    }
};
</script>

<template>
    <header :id="header" class="h-25 min-w-full"
        v-bind:class="{ 'top-0 bg-white dark:bg-slate-700 dark:text-white fixed shadow-[0_0_8px_0_rgba(0,0,0,0.3)]': !hasScroll, 'absolute top-12 lg:text-white ': hasScroll }">
        <div class="h-full container m-auto flex items-end justify-end">
            <!-- Div menu lateral droit -->
            <div :hidden="true"></div>

            <div>
                <!-- UL pour le menu lateral droit -->
                <button
                    class="cursor-pointer mb-9 text-xl leading-none px-3 py-1 border border-solid border-transparent rounded bg-transparent block lg:hidden outline-none focus:outline-none"
                    type="button" v-on:click="toggleNavbar()">
                    <font-awesome-icon :icon="['fas', 'bars']" v-bind:inverse="hasScroll" />
                </button>

                <nav v-bind:class="{ '': !showMenu, 'flex max-lg:translate-x-60': showMenu }"
                    class="lg:flex lg:flex-grow text-lg font-semibold uppercase max-lg:transform max-lg:fixed max-lg:top-0 max-lg:bottom-0 max-lg:w-60 max-lg:-left-60 max-lg:h-screen max-lg:overflow-y-auto max-lg:overflow-x-hidden max-lg:bg-white max-lg:transition max-lg:duration-500 max-lg:ease-in-out ">
                    <ul
                        class="flex flex-col lg:flex-row list-none lg:ml-auto gap-1 sm:gap-6 xl:gap-10 space-x-3 lg:space-x-10">
                        <li v-bind:class='{ "selected": selected === 0 }'
                            class="inline-block mb-3 lg:mb-9 max-lg:mt-6 max-lg:ml-3"><a href="#HomeSection"
                                v-on:click='changeSelected(0)'
                                class="transition-all duration-150 hover:border-b-4 border-red-600 hover:text-red-600"><font-awesome-icon
                                    :icon="['fas', 'home']" /></a></li>
                        <li v-bind:class='{ "selected": selected === 1 }' class="inline-block mb-3 lg:mb-9"><a
                                href="#competences" v-on:click='changeSelected(1)'
                                class="transition-all duration-150 hover:border-b-4 border-red-600 hover:text-red-600">Compétences</a>
                        </li>
                        <li v-bind:class='{ "selected": selected === 2 }' class="inline-block mb-3 lg:mb-9"><a
                                href="#activitees" v-on:click='changeSelected(2)'
                                class="transition-all duration-150 hover:border-b-4 border-red-600 hover:text-red-600">Activitées</a>
                        </li>
                        <li v-bind:class='{ "selected": selected === 3 }' class="inline-block mb-3 lg:mb-9"><a
                                href="#apropos" v-on:click='changeSelected(3)'
                                class="transition-all duration-150 hover:border-b-4 border-red-600 hover:text-red-600">A
                                propos</a></li>
                        <li v-bind:class='{ "selected": selected === 4 }' class="inline-block mb-3 lg:mb-9"><a
                                href="#contact" v-on:click='changeSelected(4)'
                                class="transition-all duration-150 hover:border-b-4 border-red-600 hover:text-red-600">Contact</a>
                        </li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>
</template>

<style scoped>
nav ul .selected a {
    border-bottom-width: 4px;
    --tw-border-opacity: 1;
    border-color: rgb(220 38 38 / var(--tw-border-opacity));
    --tw-text-opacity: 1;
    color: rgb(220 38 38 / var(--tw-text-opacity));
}
</style>
