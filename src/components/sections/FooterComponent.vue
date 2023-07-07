<template>
    <footer>
        <p>&copy; Copyright. Page created by Monika Nemcova</p>
    </footer>
</template>

<script>
export default {
    name: "FooterComponent"
}
</script>

<style>
    footer {
        display: flex;
        justify-content: center;
        padding-top: 45px;
        padding-bottom: 10px;
        color: #355070;
    }

    .dark-mode footer {
        color: #4e75a5;;
    }
</style>