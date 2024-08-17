<script>
    import start from "$img/start.png";
</script>

<slot />

<div class="task-bar">
    <div class="task-bar-left-section">
        <button class="task-bar-start-button" style="background-image: url({start});" />
    </div>

    <div class="task-bar-right-section">
    </div>
</div>
inset -100px 25px 13px -62px black;
<style>
    .task-bar {
        height: var(--task-bar-height);
        width: 100vw;
        background: #255cda;
        position: absolute;
        display: flex;
        justify-content: space-between;
        bottom: 0;
        box-shadow:
            inset 0px -58px 13px -62px black,
            inset 0px 62px 13px -62px rgb(255, 255, 255, 0.4),
            0px 22px 13px 22px black;
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

    .task-bar-left-section {
        width: 100%;
    }

    .task-bar-right-section {
        background: #0b9df0;
        height: var(--task-bar-height);
        width: 200px;
        box-shadow:
            inset 0px -58px 13px -62px black,
            inset 0px 62px 13px -62px rgb(255, 255, 255, 0.4),
            inset 62px 25px 13px -62px rgb(255, 255, 255, 0.4),
            -6px 0px 13px -3px rgba(66, 68, 90, 1);
    }
</style>