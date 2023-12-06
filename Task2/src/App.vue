<template>
    <div v-for="(accordionItem, index) in accordionItems" :key="index"> 
        <Accordion :item="accordionItem"/>
    </div>
</template>
<script>
import Accordion from './components/Accordion.vue'
export default{
    data(){
        return{
            accordionItems: [
                {
                    title: "Section 1",
                    expanded: false
                },
                 {
                    title: "Section 2",
                    expanded: false
                },
                 {
                    title: "Section 3",
                    expanded: false
                },
                 {
                    title: "Section 4",
                    expanded: false
                },
                 {
                    title: "Section 5",
                    expanded: false
                },
                 {
                    title: "Section 6",
                    expanded: false
                }

            ]
        }
    },
    components:{
      Accordion
    }
}

</script>
<style scoped>
*{
  padding: 0;
  margin:0;
}
</style>

