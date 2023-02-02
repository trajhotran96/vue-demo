<script setup>

defineProps({
    type: {
        type: String,
    },
    placeholder: {
        type: String,
        default: "Nhap..."
    },
    
})
</script>

<script>
export default {
    name: "InputComponent",
    // data() {
    //     return {
    //         icon: 
    //     }
    // },
    methods: {
        handleClickInput: (event) => {
            console.log('handleClickInput:', event)
        }
    }
}
</script>

<template>
    <div>
        <input :type="type" class="input" :placeholder="placeholder" @click="handleClickInput" />
    </div>
</template>


<style scoped>
.input {
    height: 40px;
    width: 200px;
    background-color: rgb(240, 233, 233);
    border: none;
    border-bottom: 2px solid #58c8f5;
    padding-left: 8px;
    padding-right: 8px;
    /* border:2px; */
}
.input:focus{
    outline: none;
}
</style>