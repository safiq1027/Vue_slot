<script setup>
import {ref,reactive} from 'vue'
import ButtonComponent from './components/ButtonComponent.vue';
import SlotComponent from './components/SlotComponent.vue';

const msg=ref('hello World')

function clickHandlerOne(){
    msg.value="Click One"
}

function clickHandlerTwo(){
    msg.value="Click Two"
}
</script>
<template>
    <h2> Slote</h2>
    <p class="my-2"> {{ msg }}</p>
    <p class="my-10">
        <ButtonComponent  :click-handler="clickHandlerOne" > 
           button 1
        </ButtonComponent>
    </p>
    <p class="my-10"> 
        <ButtonComponent  :click-handler="clickHandlerTwo" >
            button 2
         </ButtonComponent>
    </p>
    <SlotComponent>
        default content
        <template #header>
            <h2>This is header</h2>
        </template>
        <template v-slot:footer>
            <h2>This is footer</h2>

        </template>
    </SlotComponent>
</template>
<style scoped>
</style>