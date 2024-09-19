<script>
    import logo from "$img/logo_xp.png";

    let active = false;
</script>

<button class="task-opened">
    <img src={logo} alt="Task logo">
    <p>Notepad</p>
</button>

<style>
    .task-opened {
        background: #3a7ff4;
        width: 150px;
        height: 25px;
        margin-right: 3px;
        box-shadow:
            inset 6px 6px 13px -11px rgba(255, 255, 255, 1),
            10px 10px 20px -13px black;
        border-radius: 2px;
        border: none;
        display: flex;
        color: white;
        align-items: center;
    }

    .task-opened:hover {
        box-shadow: inset 0 0 10px 0 rgb(187, 183, 183);
    }

    .task-opened img {
        max-width: 20px;
        max-height: 20px;
        margin: 2px 4px 2px 4px;
    }
</style>