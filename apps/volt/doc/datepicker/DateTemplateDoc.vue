<template>
    <DocSectionText v-bind="$attrs">
        <p>Custom content can be placed inside date cells with the <i>date</i> slot that takes a Date as a parameter.</p>
    </DocSectionText>
    <div class="card flex justify-center">
        <DatePicker v-model="date">
            <template #date="slotProps">
                <strong v-if="slotProps.date.day > 10 && slotProps.date.day < 15" style="text-decoration: line-through">{{ slotProps.date.day }}</strong>
                <template v-else>{{ slotProps.date.day }}</template>
            </template>
        </DatePicker>
    </div>
    <DocSectionCode :code="code" />
</template>

<script setup lang="ts">
import DatePicker from '@/volt/DatePicker.vue';
import { ref } from 'vue';

const date = ref(null);

const code = ref(`
<template>
    <div class="card flex justify-center">
        <DatePicker v-model="date">
            <template #date="slotProps">
                <strong v-if="slotProps.date.day > 10 && slotProps.date.day < 15" style="text-decoration: line-through">{{ slotProps.date.day }}</strong>
                <template v-else>{{ slotProps.date.day }}</template>
            </template>
        </DatePicker>
    </div>
</template>

<script setup lang="ts">
import DatePicker from '@/volt/DatePicker.vue';
import { ref } from 'vue';

const date = ref(null);
<\/script>
`);
</script>
