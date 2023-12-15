<script>
    import PlainButton from "$lib/plainButton.svelte";
    import Noreg from "$lib/noreg.svelte";
    const towns = [
        {
            name: "Oslo",
            path: "oslobysykkel",
        },
        {
            name: "Bergen",
            path: "bergenbysykkel",
        },
        {
            name: "Trondheim",
            path: "trondheimbysykkel",
        },
    ];
</script>

<!--  center  -->
    <div class="prose text-center m-8">
        <h1>Velg din sykkel-by</h1>
        <div>
            <div
                class="w-48 pb-32 flex-col sm:justify-end justify-start items-center gap-3 inline-flex"
            >
                <div class=" w-fit h-fit">
                    <Noreg />
                </div>

                {#each towns as town}
                    <PlainButton
                        text={town.name}
                        route={`/velg-din-sykkel-by/${town.path}`}
                    />
                {/each}
            </div>
        </div>
    </div>
