<template>
    <div class="container">
        <p>{{item.title}}</p>
        <span v-if="!item.expand" class="sign" @click="expand()">+  
        </span>
        <span v-if="item.expand" class="sign" @click="expand()">-</span>
        </div>    
        <div v-if="item.expand" class="expand">
            <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Laboriosam, quos est. Hic facere autem ad, enim illo illum molestias rem beatae fuga, reprehenderit ea, dolorem a? Nostrum aut doloremque possimus!</p>
        </div>
</template>
<script>
export default {
    props:{
        item:{
            type: Object,
            required: true
        }
    },
    methods:{
        expand(){
            this.item.expand = !this.item.expand;
        }
    }
}
</script>
<style scoped>
*{
    margin:0;
    padding: 0;
    box-sizing: border-box;
}
.container{
    width: 80%;
    margin: 20px auto;
    font-size: 24px;
    display: flex;
}
.sign{
    margin-left: 10px;
    padding: 0px 5px;
    cursor:pointer;
}
.sign:hover{
    background-color: grey;
    opacity:0.4
}
.expand{
    width: 80%;
    margin: 0 auto;
}
</style>