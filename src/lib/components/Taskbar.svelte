<script>
    import logo from "$img/logo_xp.png";
</script>

<slot />

<div class="task-bar">
    <div class="task-bar-start">
        <div class="task-bar-start-content">
            <img src={logo} class="task-bar-logo" alt="Windows XP logo" />
            <p>start</p>
        </div>
    </div>
</div>

<style>
    .task-bar {
        height: var(--task-bar-height);
        width: 100vw;
        background: #255cda;
        position: absolute;
        bottom: 0;
    }

    .task-bar-start {
        height: 100%;
        width: 8rem;
        display: flex;
        align-items: center;
        background: #54ad4b;
        border-top-right-radius: 0.6rem;
        border-bottom-right-radius: 0.6rem;
    }

    .task-bar-start-content {
        display: flex;
        width: 100%;
        align-items: center;
        justify-content: center;
    }

    .task-bar-logo {
        background-color: transparent;
        height: var(--task-bar-logo-size);
        margin-right: 0.3rem;
    }

    .task-bar-start-content p {
        color: white;
        font-size: 1.2rem;
        padding-bottom: 0.1rem;
    }
</style>