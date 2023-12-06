<template>
    <div v-for="(event, index) in sortArrayAsc()" :key="index">
        <TimeLine :event="event"/>
    </div>
        
</template>
<script>
    import TimeLine from './components/TimeLine.vue'
    export default{
        data(){
            return{
                events: [
                    {
                        title: 'Assignment10',
                        date: new Date('2023-12-02'),
                        description: "NOBODY BELIEVES IN YOU YOU'VE LOST AGAIN, AGAIN AND AGAIN... THE LIGHTS ARE CUT OFF BUT YOU STILL LOOKING AT YOUR DREAM REVIEWING IT EVERY DAY AND SAY TO YOURSELF IT'S NOT OVER UNTIL I WIN",
                        isDisplayed: false
                    },
                    {
                        title: 'Assignment11',
                        date: new Date('2023-12-01'),
                        description: "NOBODY BELIEVES IN YOU YOU'VE LOST AGAIN, AGAIN AND AGAIN... THE LIGHTS ARE CUT OFF BUT YOU STILL LOOKING AT YOUR DREAM REVIEWING IT EVERY DAY AND SAY TO YOURSELF IT'S NOT OVER UNTIL I WIN",
                        isDisplayed: false
                    },
                    {
                        title: 'Assignment12',
                        date: new Date('2023-12-03'),
                        description: "NOBODY BELIEVES IN YOU YOU'VE LOST AGAIN, AGAIN AND AGAIN... THE LIGHTS ARE CUT OFF BUT YOU STILL LOOKING AT YOUR DREAM REVIEWING IT EVERY DAY AND SAY TO YOURSELF IT'S NOT OVER UNTIL I WIN",
                        isDisplayed: false
                    },
                    {
                        title: 'Assignment13',
                        date: new Date('2023-12-04'),
                        description: "NOBODY BELIEVES IN YOU YOU'VE LOST AGAIN, AGAIN AND AGAIN... THE LIGHTS ARE CUT OFF BUT YOU STILL LOOKING AT YOUR DREAM REVIEWING IT EVERY DAY AND SAY TO YOURSELF IT'S NOT OVER UNTIL I WIN",
                        isDisplayed: false
                    },
                    {
                        title: 'Assignment14',
                        date: new Date('2023-12-05'),
                        description: "NOBODY BELIEVES IN YOU YOU'VE LOST AGAIN, AGAIN AND AGAIN... THE LIGHTS ARE CUT OFF BUT YOU STILL LOOKING AT YOUR DREAM REVIEWING IT EVERY DAY AND SAY TO YOURSELF IT'S NOT OVER UNTIL I WIN",
                        isDisplayed: false
                    },

                ]
            }
        },
        components:{
            TimeLine
        },
        methods:{
            sortArrayAsc(){
                return this.events.sort((a,b) => a.date - b.date);  
            }
        }
    }

</script>

<style>

</style>
