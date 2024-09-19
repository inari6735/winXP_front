<script>
    import Taskbar from "$lib/components/Taskbar.svelte";
    import wallpaper from "$img/wallpaper.jpg";
</script>

<div class="container" style="background-image: url({wallpaper});">
    <slot />
    <Taskbar />
</div>

<style>
    .container {
        height: 100vh;
        position: relative;
        background-size: 100vw calc(100vh - var(--task-bar-height));
    }
</style>