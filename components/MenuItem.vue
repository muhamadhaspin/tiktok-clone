<script setup>
const props = defineProps(['iconString', 'colorString', 'sizeString']);
const { iconString, colorString, sizeString } = toRefs(props);

let icon = ref('');
if (iconString.value === 'For You') icon.value = 'mdi:home';
if (iconString.value === 'Following') icon.value = 'ci:group';
if (iconString.value === 'LIVE') icon.value = 'ri:live-line';
</script>

<template>
    <div class="flex w-full items-center rounded-md p-2.5 hover:bg-gray-100">
        <div class="mx-auto flex items-center lg:mx-0">
            <Icon :name="icon" :color="colorString" :size="sizeString" />

            <span
                :class="`text-[${colorString}]`"
                class="mt-0.5 hidden pl-[9px] text-[17px] font-semibold lg:block"
            >
                {{ iconString }}
            </span>
        </div>
    </div>
</template>
