<script>
    import "../app.css";
    import { fade } from 'svelte/transition';
    
</script>

<!-- <div class="bg-pink-500 w-full">
    <div class="container mx-auto max-w-lg content-center"> -->
        <div transition:fade>
            <slot />

        </div>
<!-- </div>
</div> -->
