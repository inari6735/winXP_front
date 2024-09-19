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
        background: linear-gradient(rgb(31, 47, 134) 0px, rgb(49, 101, 196) 3%, rgb(54, 130, 229) 6%, rgb(68, 144, 230) 10%, rgb(56, 131, 229) 12%, rgb(43, 113, 224) 15%, rgb(38, 99, 218) 18%, rgb(35, 91, 214) 20%, rgb(34, 88, 213) 23%, rgb(33, 87, 214) 38%, rgb(36, 93, 219) 54%, rgb(37, 98, 223) 86%, rgb(36, 95, 220) 89%, rgb(33, 88, 212) 92%, rgb(29, 78, 192) 95%, rgb(25, 65, 165) 98%);
        position: absolute;
        display: flex;
        justify-content: space-between;
        bottom: 0;
        /* box-shadow:
            inset 0px -58px 13px -62px black,
            inset 0px 62px 13px -62px rgb(255, 255, 255, 0.4),
            0px 22px 13px 22px black; */
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

    }

    .task-bar-left-section {
        width: 100%;
        display: flex;
        align-items: center;
    }

    .task-bar-right-section {
        background: linear-gradient(rgb(12, 89, 185) 1%, rgb(19, 158, 233) 6%, rgb(24, 181, 242) 10%, rgb(19, 155, 235) 14%, rgb(18, 144, 232) 19%, rgb(13, 141, 234) 63%, rgb(13, 159, 241) 81%, rgb(15, 158, 237) 88%, rgb(17, 155, 233) 91%, rgb(19, 146, 226) 94%, rgb(19, 126, 215) 97%, rgb(9, 91, 201) 100%);
        height: var(--task-bar-height);
        width: max-content;
        padding: 0 2rem 0 2rem;
        display: flex;
        align-items: center;
        justify-content: center;
    }
</style>