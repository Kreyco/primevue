<template>
    <DocSectionText v-bind="$attrs">
        <p>DatePicker provides <i>small</i> and <i>large</i> sizes as alternatives to the base.</p>
    </DocSectionText>
    <div class="card flex flex-col items-center gap-4">
        <DatePicker v-model="value1" size="small" placeholder="Small" showIcon iconDisplay="input" />
        <DatePicker v-model="value2" placeholder="Normal" showIcon iconDisplay="input" />
        <DatePicker v-model="value3" size="large" placeholder="Large" showIcon iconDisplay="input" />
    </div>
    <DocSectionCode :code="code" />
</template>

<script setup lang="ts">
import DatePicker from '@/volt/DatePicker.vue';
import { ref } from 'vue';

const value1 = ref(null);
const value2 = ref(null);
const value3 = ref(null);

const code = ref(`
<template>
    <div class="card flex flex-col items-center gap-4">
        <DatePicker v-model="value1" size="small" placeholder="Small" showIcon iconDisplay="input" />
        <DatePicker v-model="value2" placeholder="Normal" showIcon iconDisplay="input" />
        <DatePicker v-model="value3" size="large" placeholder="Large" showIcon iconDisplay="input" />
    </div>
</template>

<script setup lang="ts">
import DatePicker from '@/volt/DatePicker.vue';
import { ref } from 'vue';

const value1 = ref(null);
const value2 = ref(null);
const value3 = ref(null);
<\/script>
`);
</script>
