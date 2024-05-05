<script>
    export default {
        name: "PrimaryBtn",
        props: {
            btnText: {
                type: String,
                default: () => "Label"
            },
        },
    }
</script>

<template>

    <a class="primaryBtn">{{ btnText }}</a>

</template>

<style scoped>
    .primaryBtn {
        cursor: pointer;
        white-space: nowrap;
        background-color: transparent;
        padding: 4px 8px;
        font-size: 16px;
        font-weight: 500;
        line-height: 24px;
        text-decoration: none;
        transition: all .35s;

        border: 1px solid var(--orange);
        color: var(--orange);
        border-radius: 200px;
        justify-content: center;
        align-items: center;
        min-width: 130px;
        max-width: 130px;
        margin-left: 10px;
        margin-right: 10px;
        padding: 5px 20px;
        font-weight: 700;
        display: flex;
        
    }

    .primaryBtn:hover {
        border-width: 2px;
        border-color: var(--light-blue);
        box-shadow: 1px 1px 20px 0 var(--orange);
        border-radius: 100px;
    }
</style>
