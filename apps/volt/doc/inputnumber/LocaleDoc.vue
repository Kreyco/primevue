<template>
    <DocSectionText v-bind="$attrs">
        <p>Localization information such as grouping and decimal symbols are defined with the <i>locale</i> property which defaults to the user locale.</p>
    </DocSectionText>
    <div class="card flex flex-wrap gap-4">
        <div class="flex-auto">
            <label for="locale-user" class="font-bold block mb-2"> User Locale </label>
            <InputNumber v-model="value1" inputId="locale-user" :minFractionDigits="2" fluid />
        </div>
        <div class="flex-auto">
            <label for="locale-us" class="font-bold block mb-2"> United States Locale </label>
            <InputNumber v-model="value2" inputId="locale-us" locale="en-US" :minFractionDigits="2" fluid />
        </div>
        <div class="flex-auto">
            <label for="locale-german" class="font-bold block mb-2"> German Locale </label>
            <InputNumber v-model="value3" inputId="locale-german" locale="de-DE" :minFractionDigits="2" fluid />
        </div>
        <div class="flex-auto">
            <label for="locale-indian" class="font-bold block mb-2"> Indian Locale </label>
            <InputNumber v-model="value4" inputId="locale-indian" locale="en-IN" :minFractionDigits="2" fluid />
        </div>
    </div>
    <DocSectionCode :code="code" />
</template>

<script setup lang="ts">
import InputNumber from '@/volt/InputNumber.vue';
import { ref } from 'vue';

const value1 = ref(151351);
const value2 = ref(115744);
const value3 = ref(635524);
const value4 = ref(732762);

const code = ref(`
<template>
    <div class="card flex flex-wrap gap-4">
        <div class="flex-auto">
            <label for="locale-user" class="font-bold block mb-2"> User Locale </label>
            <InputNumber v-model="value1" inputId="locale-user" :minFractionDigits="2" fluid />
        </div>
        <div class="flex-auto">
            <label for="locale-us" class="font-bold block mb-2"> United States Locale </label>
            <InputNumber v-model="value2" inputId="locale-us" locale="en-US" :minFractionDigits="2" fluid />
        </div>
        <div class="flex-auto">
            <label for="locale-german" class="font-bold block mb-2"> German Locale </label>
            <InputNumber v-model="value3" inputId="locale-german" locale="de-DE" :minFractionDigits="2" fluid />
        </div>
        <div class="flex-auto">
            <label for="locale-indian" class="font-bold block mb-2"> Indian Locale </label>
            <InputNumber v-model="value4" inputId="locale-indian" locale="en-IN" :minFractionDigits="2" fluid />
        </div>
    </div>
</template>

<script setup lang="ts">
import InputNumber from '@/volt/InputNumber.vue';
import { ref } from 'vue';

const value1 = ref(151351);
const value2 = ref(115744);
const value3 = ref(635524);
const value4 = ref(732762);
<\/script>
`);
</script>
