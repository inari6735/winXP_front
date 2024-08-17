<script>
    import start from "$img/start.png";
  import Clock from "./Clock.svelte";
  import Task from "./Task.svelte";
</script>

<slot />

<div class="task-bar">
    <div class="task-bar-left-section">
        <button class="task-bar-start-button" style="background-image: url({start});" />
        <Task />
        <Task />
    </div>

    <div class="task-bar-right-section">
        <Clock />
    </div>
</div>

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
        margin-right: 12px;
    }

    .task-bar-start-button:hover {
        box-shadow: inset 0 0 10px 0 rgba(0, 0, 0, 0.5);
        cursor: pointer;
    }

    .task-bar-left-section {
        width: 100%;
        display: flex;
        align-items: center;
    }

    .task-bar-right-section {
        background: #0b9df0;
        height: var(--task-bar-height);
        width: max-content;
        padding: 0 2rem 0 2rem;
        display: flex;
        align-items: center;
        justify-content: center;
        box-shadow:
            inset 0px -58px 13px -62px black,
            inset 0px 62px 13px -62px rgb(255, 255, 255, 0.4),
            inset 62px 25px 13px -62px rgb(255, 255, 255, 0.4),
            -6px 0px 13px -3px rgba(66, 68, 90, 1);
    }
</style>