<template>
    <nav id="bottom-nav" :class="{dark: isActive}">
        <div>
            <a class="nav-item" :class="{dark: isActive}" href="">
                <img :src="getImage('tasks')"/>
                <span>Tasks</span>
            </a>
        </div>
        <div>
            <a class="nav-item" :class="{dark: isActive}" href="">
                <img :src="getImage('reminder')"/>
                <span>Reminders</span>
            </a>
        </div>
        <div>
            <a class="nav-item" :class="{dark: isActive}" href="">
                <img :src="getImage('calendar')"/>
                <span>Calendar</span>
            </a>
        </div>
        <div>
            <a class="nav-item" :class="{dark: isActive}" href="">
                <img :src="getImage('contacts')"/>
                <span>Contacts</span>
            </a>
        </div>
    </nav>
</template>

<script>
export default {
    name: 'BottomNav',
    data() {
    return {
      isActive: false,
      images: {
        light: {
            tasks: require('@/assets/tasks.png'),
            reminder: require('@/assets/reminder.png'),
            calendar: require('@/assets/calendar.png'),
            contacts: require('@/assets/contacts.png'),
        },
        dark: {
            tasks: require('@/assets/tasksDark.png'),
            reminder: require('@/assets/reminderDark.png'),
            calendar: require('@/assets/calendarDark.png'),
            contacts: require('@/assets/contactsDark.png'),
        }
      }
    };
  },
  mounted() {
    this.$root.$on('toggle-style', (status) => {
      this.isActive = status;
    })
  },
  methods: {
    getImage(service) {
        return this.isActive ? this.images.dark[service] : this.images.light[service];
    }
  },
  inject: ['toggleStyle'],
}
</script>

<style>
#bottom-nav {
    align-items: center;
    height: 5.4vh;
    padding: 10px;
    display: flex;
    justify-content: space-evenly;
    position: fixed;
    bottom: 0;
    width: 100%;
    background-color: hsl(0, 0%, 96%);
}
#bottom-nav.dark {
    background-color: #263754;
}
.nav-item {
    display: flex;
    flex-direction: column;
    align-items: center;
    font-size: 12px;
    text-decoration: none;
    color: black;
}
.nav-item.dark {
    color: white;
}
.nav-item img {
    max-height: 22px;
    width: auto;
    padding-bottom: 5px;
}

</style>