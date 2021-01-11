<template>
    <i id="style-changer" class="icon-sun" @click="changeMode"></i>
</template>

<script>
export default {
    name: "ModeChanger",
    data() {
        return {
            isDarkMode: true,
        }
    },
    methods: {
        changeMode() {
            if (this.isDarkMode) {
                document.getElementById("style-changer").className = "icon-moon-inv"
                document.body.style.backgroundColor = "#ffffff"
                document.getElementById("clock").style.color = "#000000"
                document.getElementById("date").style.color = "#000000"
                this.isDarkMode = false
            } else {
                document.getElementById("style-changer").className = "icon-sun"
                document.body.style.backgroundColor = "#121212"
                document.getElementById("clock").style.color = "#ffffff"
                document.getElementById("date").style.color = "#ffffff"
                this.isDarkMode = true
            }
        }
    }
}
</script>

<style scoped>
.icon-sun {
    font-size: 30px;
    color: white;
}

.icon-sun:hover {
    cursor: pointer;
}

.icon-moon-inv {
    font-size: 30px;
    color: black;
}

.icon-moon-inv:hover {
    cursor: pointer;
}
</style>