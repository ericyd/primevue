<template>
    <DocSectionText v-bind="$attrs">
        <p>PrimeVue plugin is required to be installed as an application plugin to set up the default <NuxtLink to="/configuration">configuration</NuxtLink>. The plugin is lightweight, and only utilized for configuration purposes.</p>
    </DocSectionText>
    <DocSectionCode :code="code" hideToggleCode importCode hideStackBlitz />
</template>

<script>
export default {
    data() {
        return {
            code: {
                basic: `
import { createApp } from 'vue';
import PrimeVue from 'primevue/config';

const app = createApp(App);
app.use(PrimeVue);
`
            }
        };
    }
};
</script>
