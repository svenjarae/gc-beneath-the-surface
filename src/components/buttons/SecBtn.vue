<script>
    export default {
        name: "SecBtn",
        props: {
            btnText: {
                type: String,
                default: () => "Label"
            },
        },
    }
</script>

<template>

    <a class="secBtn">{{ btnText }}</a>

</template>

<style scoped>
    .secBtn {
        cursor: pointer;
        background-color: var(--orange);
        color: #fff;
        text-align: center;
        border-radius: 100px;
        justify-content: center;
        align-items: center;
        min-width: 130px;
        max-width: 200px;
        padding: 5px 20px;
        font-size: 16px;
        font-weight: 600;
        line-height: 24px;
        text-decoration: none;
        transition: all .5s;
        display: flex;
    }

    .secBtn:hover {
        background-color: var(--silver);
        color: var(--black);
    }
</style>
