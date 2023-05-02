<script>

export default {
    name: 'DaysInMonth',
    props: {
        year: String,
        month: String
    },
    data() {
        return {
            count: 1
        }
    },
    mounted() {

    },
    methods: {
        getDaysInMonth() {
            let date = new Date(this.date);
            let year = date.getFullYear();
            let month = date.getMonth();
            return new Date(year, month + 1, 0).getDate();
        },
        /**
         * @param {int} The month number, 0 based
         * @param {int} The year, not zero based, required to account for leap years
         * @return {Date[]} List with date objects for each day of the month
         */
        getDaysInMonthS(month, year) {
            let date = new Date(year, month, 1);
            let days = [];
            while (date.getMonth() === month) {
                days.push(new Date(date));
                date.setDate(date.getDate() + 1);
            }
            return days;
        }
    },
}

</script>

<template>
    <div class='greetings'>
        <h1 class='green'>{{ msg }}</h1>
        <h3>
            You’ve successfully created a project with
            <a href='https://vitejs.dev/' target='_blank' rel='noopener'>Vite</a> +
            <a href='https://vuejs.org/' target='_blank' rel='noopener'>Vue 3</a>.
        </h3>
    </div>
</template>

<style scoped>
h1 {
    font-weight: 500;
    font-size: 2.6rem;
    top: -10px;
}

h3 {
    font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
    text-align: center;
}

@media (min-width: 1024px) {
    .greetings h1,
    .greetings h3 {
        text-align: left;
    }
}
</style>
