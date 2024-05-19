<script>

import { RouterLink } from 'vue-router'
import PrimaryBtn from '@/components/buttons/PrimaryBtn.vue';
import SecBtn from '@/components/buttons/SecBtn.vue';


export default {
    components: {
        PrimaryBtn,
        SecBtn,
    },

}

</script>

<template>
    <header>
        <div class="navContainer">
            <div class="wrapper">
                <nav>
                    <img alt="logo" class="logo" width="120" height="auto" />
                    <RouterLink to="/methods">Methods</RouterLink>
                    <RouterLink to="/team">Team</RouterLink>
                    <RouterLink to="/advantages">Advantages</RouterLink>
                </nav>
            </div>
            <div class="btnWrapper">
                <PrimaryBtn ></PrimaryBtn>
                <SecBtn></secBtn>
            </div>
        </div>
    
    </header>

</template>

<style scoped>

    .navContainer{
        display: flex;
        justify-content: space-between;
        align-items: center;
        z-index: 2;
        position: fixed;
        right: 0;
        left: 0;
        max-width: 1300px;
        margin: auto;
        z-index: 9;
        background-color: var(--black);
        color: var(--silver);
        align-items: center;
        width: 100%;
        min-height: 10vh;
        max-height: 15vh;
        padding: 24px 5%;
        display: flex;
        position: fixed;
    }

    nav a{
        vertical-align: top;
        color: #222;
        text-align: left;
        margin-left: auto;
        margin-right: auto;
        padding: 20px;
        text-decoration: none;
        display: inline-block;
        position: relative;

        color: var(--silver);
        white-space: nowrap;
        background-color: transparent;
        padding: 4px 8px;
        font-size: 16px;
        font-weight: 500;
        line-height: 24px;
        text-decoration: none;
        transition: all .35s;
    }

    nav a:hover{
        color: var(--orange);
    }

    .wrapper nav{
        grid-column-gap: 32px;
        grid-row-gap: 32px;
        align-items: center;
        display: flex;
        position: static;
    }

    .btnWrapper{
        grid-column-gap: 8px;
        align-items: center;
        display: flex;
    }

</style>
