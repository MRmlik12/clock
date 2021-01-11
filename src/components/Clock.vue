<template>
    <a id="clock">{{ hours }}:{{ minutes }}:{{ seconds }}</a>
    <a id="date">{{ day }}, {{ month }} {{ year }}</a>  
</template>

<script>
export default {
    name: "Clock",
    data() {
        return {
            hours: null,
            minutes: null,
            seconds: null,
            day: null,
            month: null,
            year: null
        }
    },
    mounted() {
        setInterval(this.updateTime, 1000)
    },
    methods: {
        updateTime() {
            let date = new Date()
            this.hours = (date.getHours() < 10)? "0" + date.getHours():date.getHours()
            this.minutes = (date.getMinutes() < 10)? "0" + date.getMinutes():date.getMinutes()
            this.seconds = (date.getSeconds() < 10)? "0" + date.getSeconds():date.getSeconds()
            this.day = date.getDate()
            this.month = this.getMonthShortName(date.getMonth())
            this.year = date.getFullYear()
        },
        getMonthShortName(month) {
            const months = ["Jan", "Feb", " Mar", "Apr", "May", "Jun", "Jul", "Aug", "Sep", "Oct", "Nov", "Dec"] 
            return months[month]
        }
    }
}
</script>

<style scoped>
#clock {
    font-size: 90px;
    
}

#date {
    margin-left: 5px;
    font-size: 29px;
}
</style>