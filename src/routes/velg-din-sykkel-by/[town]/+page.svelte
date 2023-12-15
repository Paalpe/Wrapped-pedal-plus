<script>
    import { onMount } from 'svelte';
    import PlainButton from "$lib/plainButton.svelte";
    import JSZip from 'jszip';
    export let data;

    const href = `https://${data.slug}.no/profil/dine-data`;

    /**
     * @type {HTMLInputElement}
     */
    let fileInput;
    onMount(() => {
        fileInput.onchange = function () {
            var zip = new JSZip();
            // @ts-ignore
            zip.loadAsync(this.files[0]).then(
                function (zip) {
                    console.log(zip);
                    // process ZIP file content here
                    alert("OK");
                },
                function () {
                    alert("Not a valid zip file");
                },
            );
        };
    });
</script>

<div class="prose text-start m-8">
    <h1 class="text-center">Hent og last opp årets turer</h1>
    <div class="flex justify-center">
        <div class="max-w-xs text-lg text-start">
            <p>
                <b>1.</b> Last ned turer fra
                <a class="text-red-600" {href}>{data.slug}.no</a>
            </p>

            <div class="p-8"></div>
            <p>2. Last opp <span class="text-red-600">.zip filen</span></p>

            <div class="text-center">
                <PlainButton text="Velg fil" />
            </div>
            <input type="file" bind:this={fileInput} />

            <div class="">
                <span style="text-black text-xs font-light font-['SF Pro Text']"
                    >Turene dine wrappes opp lokalt! - altså
                </span><span
                    style="text-black text-xs font-bold font-['SF Pro Text']"
                    >ingen data blir laget her</span
                >
            </div>
        </div>
    </div>
</div>
