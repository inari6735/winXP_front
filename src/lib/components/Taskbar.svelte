<script>
    import start from "$img/start.png";
</script>

<slot />

<div class="task-bar">
    <button class="task-bar-start-button" style="background-image: url({start});" />
</div>

<style>
    .task-bar {
        height: var(--task-bar-height);
        width: 100vw;
        background: #255cda;
        position: absolute;
        bottom: 0;
    }

    .task-bar-start-button {
        border: none;
        height: var(--task-bar-height);
        width: var(--start-button-width);
        background: transparent;
    }

    .task-bar-start-button:hover {
        box-shadow: inset 0 0 10px 0 rgba(0, 0, 0, 0.5);
        cursor: pointer;
    }

</style>