<script setup>
const route = useRoute()
console.log(route)
const router = useRouter()
console.log(router)
const { data } = await useAsyncData('blogs', () => queryContent('/blogs').find())
useHead({
    meta: [
        {
            name: 'description',
            content: 'Developer Counts is a blog about software development, and other things.'
        },
        {
            name: 'keywords',
            content: 'software development, blog, developer counts, ceo'
        }
    ]
})
</script>
<template>
<main>
    <h1>Main Feeling About Coding</h1>
    <div v-for="blog in data">
        <h1>{{blog.title}}</h1>
    </div>
</main>
</template>