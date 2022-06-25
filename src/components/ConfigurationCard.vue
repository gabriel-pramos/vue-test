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
                <div class="text-overline mb-3">
                CONFIGURAÇÃO
                </div>

                <v-list>
                    <v-list-item>
                        <v-btn
                            class="mx-2"
                            elevation="3"
                            outlined
                            width="100%"
                        >
                            <v-icon dark> mdi-autorenew </v-icon>
                            Alterar API Key
                        </v-btn>
                    </v-list-item>
                </v-list>

            </v-list-item-content>
        </v-list-item>

    </v-card>
</template>

<script>
    export default {
        data: () => ({
            credit: Math.round(Math.random()*100000),
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