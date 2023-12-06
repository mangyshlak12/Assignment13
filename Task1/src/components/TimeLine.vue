<template>
    <div class="container" @click="displayInf()">
        <p>{{event.title}}</p>
        <span class="date">{{event.date.toLocaleDateString()}}</span>
        <div v-if="event.isDisplayed">
            
            <p class="description">{{event.description}}</p>
        </div>
    </div>
</template>
<script>
    export default{
        data(){
            return{
                
            }
        },
        props:{
            event:{
                type: Object,
                required: true
            }
        },
        methods:{
            displayInf(){
                console.log('hello');
                this.event.isDisplayed = !this.event.isDisplayed;
            }
        }
    }
</script>
<style scoped>
*{
    margin:0;
    padding:0;
    box-sizing: border-box;
}
.container{
    background-color: hotpink;
    width: 80%;
    margin: 0 auto;
    text-align: center;
    padding: 15px 0px;
    margin-bottom: 10px;
    font-size: 22px;
    border-radius: 10px;
}
.container:hover{
    transform: scale(1.1);
    cursor: pointer;
}
.date{
    font-size: 16px;
    color:  green;
    font-weight: 600;
}
.description{
    font-size:18px;
    color: #332d2c;
}
</style>
