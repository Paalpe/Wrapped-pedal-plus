<script>
    	import { fade } from 'svelte/transition';
        import PlainButton from '$lib/plainButton.svelte';
</script>
<div class="bg-pink-500 w-full">
    <div class="container mx-auto max-w-lg content-center">

        <div class="h-screen content-center flex justify-center">
            <div class="w-72 h-80 relative">
                <div class="w-16 h-16 left-[116px] top-0 absolute"></div>
                <div  transition:fade={{ delay: 250, duration: 300 }} 
                    class="w-72 left-0 top-[54px] absolute text-center text-white text-9xl font-bold font-['Trebuchet MS']"
                >
                    2023
                </div>
                <div
                    class="w-72 left-0 top-[179px] absolute text-center text-white text-6xl font-bold font-['Trebuchet MS']"
                >
                    WRAPPED
                </div>
                <!-- <div class="w-52 h-5 left-[1px] top-[323px] absolute bg-black"></div> -->
                <div
                    class="w-72 left-0 top-[277px] absolute opacity-95 self-stretch flex-col justify-start items-center gap-12 inline-flex"
                >
                    <span
                        style="text-black text-base font-normal font-['Trebuchet MS'] leading-snug"
                        >En helt unødvendig nødvendighet for både deg som har
                        bysykklet litt, og for
                        <span
                            class="before:block before:absolute before:-inset-1 before:bg-black relative inline-block"
                        >
                            <span class="relative text-white"
                                >deg som elsker å bysykkle!</span
                            >
                        </span>
                    </span><span
                        style="before:block before:absolute before:-inset-1 before:-skew-y-3 before:bg-pink-500 text-white text-base font-bold font-['Trebuchet MS'] leading-snug"
                    ></span><span
                        style="text-black text-base font-bold font-['Trebuchet MS'] leading-snug"
                    >
                    </span>
                    <PlainButton text="Få din Wrapped" route="/velg-din-sykkel-by" />
                   
                </div>
            </div>
        </div>
    </div>
</div>
