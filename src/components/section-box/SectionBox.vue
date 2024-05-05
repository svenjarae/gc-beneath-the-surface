<script setup>

</script>

<template>
    <div class="outerContainer">
        <h1 class="title">Placeholder title</h1>
        <h2 class="subtitle">Placeholder subtitle</h2>
        <p class="text">Placeholder Text Lorem ipsum.</p>
    </div>
</template>

<style scoped>

    .outerContainer{
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        text-align: center;
    }

    .title {
        color: var(--silver);
        margin-bottom: 5px;
        font-family: Big Shoulders Display, sans-serif;
        font-size: 4.2rem;
        font-weight: 500;
        line-height: 4.4rem;
        text-transform: uppercase;
    }

    .subtitle {
        letter-spacing: 2px;
        text-transform: uppercase;
        font-family: DM Sans, sans-serif;
        font-size: 1.3rem;
        font-weight: 700;
        line-height: 1.5rem;
        font-weight: 700;
        color: var(--grey);
        margin-bottom: 10px;
    }

    .text {
        z-index: 10;
        text-align: center;
        white-space: break-spaces;
        color: var(--silver);
        margin-bottom: 10px;
        line-height: 1.4rem;
        letter-spacing: .5px;
        margin-top: 10px;
        font-size: 1rem;
    }
</style>
