<template>
    <v-card
        elevation="3"
        :loading="loading"
        class="mx-auto my-12"
        max-width="550"
        outlined
    >
        <v-list-item two-line>
            <v-list-item-content>
                <div class="text-overline">
                CRÉDITOS
                </div>

                <p class="text-h1 text--primary text-center">
                    {{ credit }}
                </p>

                <v-btn plain @click="credit = Math.round(Math.random()*10000)">Adicinar mais</v-btn>

            </v-list-item-content>
        </v-list-item>

    </v-card>
</template>

<script>
    export default {
        data: () => ({
            credit: Math.round(Math.random()*10000),
            loading: false,
            selection: 1,
        }),

        methods: {
            reserve () {
                this.loading = true
                setTimeout(() => (this.loading = false), 2000)
            },
        },
    }
</script>

<style>
.big-font {
    font-size: 2rem;
}
</style>