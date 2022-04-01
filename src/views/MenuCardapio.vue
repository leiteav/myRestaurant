<template>
<p>
{{ test }}
</p>
</template>
<script lang="ts">
import { defineComponent } from 'vue';
export default defineComponent({
name: "MenuCardapio",
data() {
    return {
        test: "teste"
    }
},
methods:{

}

});
</script>
<style scoped>
p {
    color: white;
}
</style>
