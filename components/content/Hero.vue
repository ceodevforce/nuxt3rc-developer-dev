<script setup>
defineProps({
    title: {
        type: String,
        default: 'Developer Counts'
    }  
})
</script>
<template>
<div>
    <main>
        <h1>{{title}}</h1>
        <slot/>
    </main>
</div>
</template>