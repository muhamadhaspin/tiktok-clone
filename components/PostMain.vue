<script setup>
let video = ref(null);

onMounted(() => video.value.play());
</script>

<template>
    <div id="PostMain" class="flex border-b py-6">
        <div class="cursor-pointer">
            <img
                src="https://picsum.photos/id/8/300/320"
                alt="user profile"
                width="60"
                class="max-h-[60px] rounded-full"
            />
        </div>

        <div class="w-full px-4 pl-3">
            <div class="flex items-center justify-between pb-0.5">
                <button>
                    <span class="cursor-pointer font-bold hover:underline">
                        User name
                    </span>

                    <span
                        class="text-light cursor-pointer pl-1 text-[13px] text-gray-500"
                    >
                        User name
                    </span>
                </button>

                <button
                    class="rounded-md border border-primary px-[21px] py-0.5 text-[15px] font-semibold text-primary hover:bg-[#ffeef2]"
                >
                    Follow
                </button>
            </div>

            <div
                class="max-w-[300px] break-words pb-0.5 text-[15px] md:max-w-[400px]"
            >
                This is some text
            </div>

            <div class="pb-0.5 text-[14px] text-gray-500">
                #fun #cool #superAwesome
            </div>

            <div class="flex items-center pb-0.5 text-[14px] font-semibold">
                <Icon name="mdi:music" size="17" />

                <div class="px-1">original sound - AWESOME</div>

                <Icon name="mdi:heart" size="20" />
            </div>

            <div class="mt-2.5 flex">
                <div
                    class="relative flex max-h-[580px] min-h-[480px] max-w-[260px] cursor-pointer items-center rounded-xl bg-black"
                >
                    <video
                        src="/animal.mp4"
                        ref="video"
                        class="mx-auto h-full rounded-xl object-cover"
                        loop
                        muted
                    />

                    <img
                        src="~/assets/images/tiktok-logo-white.png"
                        alt="logo white"
                        width="90"
                        class="absolute bottom-14 right-2"
                    />
                </div>

                <div class="relative mr-[75px]">
                    <div class="absolute bottom-0 pl-2">
                        <div class="pb-4 text-center">
                            <button
                                class="cursor-pointer rounded-full bg-gray-200 p-2"
                            >
                                <Icon name="mdi:heart" size="25" />
                            </button>

                            <span class="text-xs font-semibold text-gray-800">
                                35
                            </span>
                        </div>

                        <div class="pb-4 text-center">
                            <button
                                class="cursor-pointer rounded-full bg-gray-200 p-2"
                            >
                                <Icon
                                    name="bx:bxs-message-rounded-dots"
                                    size="25"
                                />
                            </button>

                            <span class="text-xs font-semibold text-gray-800">
                                35
                            </span>
                        </div>

                        <div class="pb-4 text-center">
                            <button
                                class="cursor-pointer rounded-full bg-gray-200 p-2"
                            >
                                <Icon name="ri:share-forward-fill" size="25" />
                            </button>

                            <span class="text-xs font-semibold text-gray-800">
                                35
                            </span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
