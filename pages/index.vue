<template>
    <main>
        <section>
            <h1>Welcome to Developer Counts</h1>
            <h3>Hi, my name is CEo!</h3>
        </section>
        <section>
            <h1>Blogs</h1>
            <ContentList path="/blogs" v-slot="{ list }">
                <div v-for="article in list" :key="article._path">
                    <h2>
                        <NuxtLink :to="article._path">{{ article.title }}</NuxtLink>
                    </h2>
                    <p>{{ article.description }}</p>
                </div>
            </ContentList>
        </section>
        <section>
            <h1>Projects</h1>
            <ContentList path="/articles" v-slot="{ list }">
                <div v-for="project in list" :key="project._path">
                    <h2>{{ project.title }}</h2>
                    
                </div>
            </ContentList>
        </section>
    </main>
</template>