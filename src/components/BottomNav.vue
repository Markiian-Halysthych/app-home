<template>
    <nav class="bottom-nav">
        <div>
            <a class="nav-item" href="">
                <img src="@/assets/tasks.png"/>
                <span>Tasks</span>
            </a>
        </div>
        <div>
            <a class="nav-item" href="">
                <img src="@/assets/reminder.png"/>
                <span>Reminders</span>
            </a>
        </div>
        <div>
            <a class="nav-item" href="">
                <img src="@/assets/calendar.png"/>
                <span>Calendar</span>
            </a>
        </div>
        <div>
            <a class="nav-item" href="">
                <img src="@/assets/contacts.png"/>
                <span>Contacts</span>
            </a>
        </div>
    </nav>
</template>

<script>
export default {
    name: 'BottomNav'
}
</script>

<style>
.bottom-nav {
    padding-top: 10px;
    padding-bottom: 10px;
    display: flex;
    justify-content: space-evenly;
    position: fixed;
    bottom: 0;
    width: 100%;
    background-color: hsl(0, 0%, 96%);
}
.nav-item {
    display: flex;
    flex-direction: column;
    align-items: center;
    font-size: 12px;
    text-decoration: none;
    color: black;
}
.nav-item img {
    max-height: 22px;
    width: auto;
    padding-bottom: 5px;
}

</style>