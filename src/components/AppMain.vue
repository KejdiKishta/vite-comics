<!-- *Descrizione:
Continuate a lavorare nella stessa repo di ieri e create un nuovo componente per visualizzare le card dei fumetti, prendendo i dati dal file json che trovate in allegato.
Una volta inseriti tutti i contenuti dinamicamente, completate il vostro layout e rifinite i dettagli con Sass. -->

<script>
export default {
    data() {
        return {

        }
    }
}
</script>

<template>
    <main>
        <div class="container">
            <h2>Penso di non aver mai visto un film della DC comics &#x1F440;</h2>
        </div>
    </main>
</template>

<style scoped lang="scss">
    @use "../style/partials/variables" as *;

    main {
        padding: 50px;
        background-color: $black-color;
        
        h2 {
            color: $white-color;
        }
    }

</style>