<script setup>
import DatepickerIcon from './DatepickerIcon.vue';
defineProps({
    label: {
        type: String,
        required: true,
        default: "Label"
    },
    noteLabel: {
        type: String
    },
    type: {
        type: String
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
    <div class="container">
        <div class="label-container">
            <span class="font-label">{{label}}</span>
            <span v-if="noteLabel != undefined" class="font-note-label">{{noteLabel}}</span>
        </div>
        <div class="form-container">
            <div class="icon-container"><DatepickerIcon class="icon-date"/></div>
            <input :type="type" class="input" :placeholder="placeholder" @click="handleClickInput" />
        </div>
    </div>
</template>


<style scoped>
.container {
    margin: 0px 0px 16px 0px;
}

.label-container {

}

.font-label {
    font-size: 18px;
    color: #3490f2;
}

.font-note-label {
    margin-left: 10px;
    padding: 0px 4px 0px 4px;
    background-color: #3490f2;
    border-radius: 4px;
    color: #fff;
}

.form-container {
    align-items: center;
    display: flex;
    flex-flow: row;
    margin: 8px 0px 0px 0px;
}
.input {
    height: 40px;
    width: 200px;
    background-color: rgb(240, 233, 233);
    border: none;
    border-bottom: 2px solid #58c8f5;
    padding-left: 8px;
    padding-right: 8px;
}
.input:focus{
    outline: none;
}
.icon-container {
    height: 20px;
    width: 20px;
    margin-right: 8px;
}
.icon-date {
    height: 20px;
    width: 20px;
}
</style>