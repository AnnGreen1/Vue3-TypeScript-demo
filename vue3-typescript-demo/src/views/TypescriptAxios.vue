<template>
    <div>

    </div>
</template>

<script  lang="ts" setup>
import { reactive, ref, onMounted } from "vue";
import { randqinghua } from '@/api/api'

const data = ref(1);
const object = reactive({
    name:"name",
    age:0
})


onMounted(() => {
    let randqinghua_data = { 'format': 'json' }
    randqinghua(randqinghua_data).then((res) => {
        console.log(res)
    }).catch((error) => {
        console.log(error);
    })
});


</script>