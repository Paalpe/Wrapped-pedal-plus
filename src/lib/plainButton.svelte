<script>
    import { goto } from "$app/navigation";

    export let text = "Få din Wrapped";
    export let route = "/";

    function navigate() {
        goto(route);
    }
    

</script>
<button
    on:click={navigate}
    class="min-w-[200px] px-12 py-3.5 hover:bg-gray-900 bg-black rounded-3xl justify-center items-center gap-2.5 inline-flex"
>
    <div class="text-white text-center text-base font-bold font-['Trebuchet MS']">
        {text}
    </div>
</button>