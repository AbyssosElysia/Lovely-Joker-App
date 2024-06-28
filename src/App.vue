<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
import MainAsideBar from '@/components/MainAsideBar.vue'
import MainHeader from '@/components/MainHeader.vue'
import ExampleForm from '@/components/ExampleForm.vue'
</script>

<template>
    <!--                <header>
                <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" />

                <div class="wrapper">
&lt;!&ndash;                    <HelloWorld msg="You did it!" />&ndash;&gt;


                </div>
            </header>-->

    <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
        <RouterLink to="/login">login</RouterLink>/
    </nav>

    <RouterView />

    <!--        <main-aside-bar></main-aside-bar>-->

    <!--        <main-header></main-header>-->

    <!--    <el-container>
        <main-aside-bar></main-aside-bar>

        <el-container direction="vertical" style="flex: 1">
            <main-header></main-header>
            <example-form></example-form>
        </el-container>
    </el-container>-->
</template>

<style scoped>
header {
    line-height: 1.5;
    max-height: 100vh;
}

.logo {
    display: block;
    margin: 0 auto 2rem;
}

nav {
    width: 100%;
    font-size: 12px;
    text-align: center;
    margin-top: 2rem;
}

nav a.router-link-exact-active {
    color: var(--color-text);
}

nav a.router-link-exact-active:hover {
    background-color: transparent;
}

nav a {
    display: inline-block;
    padding: 0 1rem;
    border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
    border: 0;
}

@media (min-width: 1024px) {
    header {
        display: flex;
        place-items: center;
        padding-right: calc(var(--section-gap) / 2);
    }

    .logo {
        margin: 0 2rem 0 0;
    }

    header .wrapper {
        display: flex;
        place-items: flex-start;
        flex-wrap: wrap;
    }

    nav {
        text-align: left;
        margin-left: -1rem;
        font-size: 1rem;

        padding: 1rem 0;
        margin-top: 1rem;
    }
}

el-container {
    height: 100vh; /* 使容器充满屏幕高度 */
}

main-header,
example-form {
    flex: none; /* 防止组件自适应高度 */
}
</style>
