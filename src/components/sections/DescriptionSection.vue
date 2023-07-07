<template>
    <section class="description">
        <h1>Hi, I'm Monika</h1>
        <h3>Welcome to my page</h3>
    </section>
</template>

<script>
export default {
    name: "DescriptionSection"
}
</script>

<style>
    .description {
        padding: 4% 10%;
        color: #355070;
        /* color: #4b71a0; */
    }

    .description h1 {
        font-size: 100px;
        display: flex;
        width: 100%;
        letter-spacing: 9px;
    }

    .description h3 {
        font-size: 40px;
        padding-top: 20px;
        display: flex;
        letter-spacing: 5px;
    }

    /***** DARK MODE *****/
    .dark-mode .description {
        color:#456894;
    }
</style>