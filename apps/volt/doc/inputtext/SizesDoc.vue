<template>
    <DocSectionText v-bind="$attrs">
        <p>InputText provides <i>small</i> and <i>large</i> sizes as alternatives to the base.</p>
    </DocSectionText>
    <div class="card flex flex-col items-center gap-4">
        <InputText v-model="value1" type="text" size="small" placeholder="Small" />
        <InputText v-model="value2" type="text" placeholder="Normal" />
        <InputText v-model="value3" type="text" size="large" placeholder="Large" />
    </div>
    <DocSectionCode :code="code" />
</template>

<script setup lang="ts">
import InputText from '@/volt/InputText.vue';
import { ref } from 'vue';

const value1 = ref(null);
const value2 = ref(null);
const value3 = ref(null);

const code = ref(`
<template>
    <div class="card flex flex-col items-center gap-4">
        <InputText v-model="value1" type="text" size="small" placeholder="Small" />
        <InputText v-model="value2" type="text" placeholder="Normal" />
        <InputText v-model="value3" type="text" size="large" placeholder="Large" />
    </div>
</template>

<script setup lang="ts">
import InputText from '@/volt/InputText.vue';
import { ref } from 'vue';

const value1 = ref(null);
const value2 = ref(null);
const value3 = ref(null);
<\/script>
`);
</script>
