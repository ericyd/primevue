<template>
    <DocComponent title="Vue Fieldset Component" header="Fieldset" description="Fieldset is a collapsible container component." :componentDocs="docs" />
</template>

<script setup lang="ts">
import BasicDoc from '@/doc/fieldset/BasicDoc.vue';
import DownloadDoc from '@/doc/fieldset/DownloadDoc.vue';
import ImportDoc from '@/doc/fieldset/ImportDoc.vue';
import TemplateDoc from '@/doc/fieldset/TemplateDoc.vue';
import ToggleableDoc from '@/doc/fieldset/ToggleableDoc.vue';
import { ref } from 'vue';

const docs = ref([
    {
        id: 'dowload',
        label: 'Download',
        component: DownloadDoc
    },
    {
        id: 'import',
        label: 'Import',
        component: ImportDoc
    },
    {
        id: 'basic',
        label: 'Basic',
        component: BasicDoc
    },
    {
        id: 'toggleable',
        label: 'Toggleable',
        component: ToggleableDoc
    },
    {
        id: 'template',
        label: 'Template',
        component: TemplateDoc
    }
]);
</script>
