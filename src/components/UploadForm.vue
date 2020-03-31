<template>
    <div class="dropArea">
        <input 
        class="dropInput"
        type="file" 
        @change="uploadImages($event.target.files)"
        multiple
        accept="image/*" />
        <span>Drag files here</span>
    </div>
</template>

<script>
import { mapActions } from 'vuex';

export default {
    name: 'UploadForm',
    methods:{
        ...mapActions(['uploadImages'])
    },
};
</script>

<style scoped>
.dropArea{
    height: 30vh;
    border: 5px dashed salmon;
    border-radius: 5px;
    display: flex;
    justify-content: center;
    align-items: center;
    position: relative;
}

.dropArea:hover{
    background-color: pink;
}

.dropInput{
    width: 100%;
    height: 30vh;
    position: absolute;
    opacity: 0%;
}
</style>