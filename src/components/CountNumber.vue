<template>
    <div>
        <p class="num">{{number}}</p>
    </div>
</template>
<script lang="ts" setup>
    const props = defineProps({//コンポーネント呼び出し時にtextでString型受け取り
        number: Number
    })
</script>

<style scoped>
    .num{
        font-size: 60px;
    }
</style>
