<script>

import { RouterLink } from 'vue-router'

export default {
    components: {

    },

}

</script>

<template>
    <footer>
        <div class="thinLine"></div>
        <div class="footerContainer">
            
            <div class="footerWrapper">
                <ul>
                    <li class="listHeader">Headline</li>
                    <li class="footerLink">One</li>
                    <li class="footerLink">Two</li>
                </ul>
                <ul>
                    <li class="listHeader">Headline</li>
                    <li class="footerLink">One</li>
                    <li class="footerLink">Two</li>
                </ul>
                <ul>
                    <li class="listHeader">Headline</li>
                    <li class="footerLink">One</li>
                    <li class="footerLink">Two</li>
                </ul>
                <ul>
                    <li class="listHeader">Headline</li>
                    <li class="footerNewsletter">
                        <p>
                            <strong>Email:</strong>&nbsp;
                            <a class="link" href="mailto:info@placeholder.com">info@placeholder.com</a><br>
                            <strong>Phone:</strong>&nbsp;+00 1234 56789
                        </p>
                    </li>
                </ul>
            </div>
            <div>
                <a href="https://maps.app.goo.gl/5ePbQYtVA17Eab2R8?g_st=ic" target="_blank" class="footerContactLink">
                    <img src="https://assets-global.website-files.com/62f41751b9b8311f542dbcf9/632388518453c317369ce51b_pin.png" loading="lazy" sizes="(max-width: 991px) 24px, (max-width: 1279px) 2vw, 24px" srcset="https://assets-global.website-files.com/62f41751b9b8311f542dbcf9/632388518453c317369ce51b_pin-p-500.png 500w, https://assets-global.website-files.com/62f41751b9b8311f542dbcf9/632388518453c317369ce51b_pin.png 512w" alt="" class="icon">
                    <div class="thin-text">Gran Canaria Beneath the surface|&nbsp;EL-33, J-Block, MIDC&nbsp;Bhosari, Pune 411026, Pune MH, <strong>Canary Islands</strong><span></span></div>
                </a>
            </div>
        </div>
    </footer>
</template>

<style scoped>
    .thinLine{
        background-color: rgba(170, 170, 170, .3);
        width: 100%;
        height: 1px;
        margin-bottom: 100px;
        margin-top: 100px;
    }

    .footerWrapper{
        display: grid;
        grid-column-gap: 24px;
        grid-row-gap: 24px;
        grid-template-rows: auto;
        grid-template-columns: 1fr 1fr 1fr 2fr;

        
    }

    .footerContainer{
        z-index: 2;
        background-color: #000;
        padding: 0 5% 48px;
        position: relative;
    }

    .footerContactLink {
        color: #c8c9d0;
        background-color: #111218;
        border: 1px solid #22242f;
        border-radius: 50px;
        justify-content: flex-start;
        align-items: center;
        max-width: 500px;
        min-height: 48px;
        margin-top: 40px;
        margin-bottom: 32px;
        padding: 8px 24px;
        font-size: 12px;
        font-weight: 600;
        line-height: 16px;
        text-decoration: none;
        display: flex;
    }

    .listHeader{
        color: #f4f4f6;
        letter-spacing: -.02em;
        margin-bottom: 32px;
        font-size: 18px;
        font-weight: 700;
        line-height: 24px;
    }

    .footerLink {
        color: #b2b3bd;
        margin-top: 8px;
        margin-bottom: 8px;
        padding-top: 4px;
        padding-bottom: 4px;
        font-size: 16px;
        font-weight: 300;
        text-decoration: none;
        transition: all .3s, opacity .2s;
        display: block;
    }

    .footerNewsletter {
        background-color: var(--glass-black);
        border-radius: 48px;
        flex-direction: column;
        justify-content: center;
        align-items: flex-start;
        width: 100%;
        height: auto;
        padding: 5% 5% 5% 10%;
        display: flex;
        color: var(--grey);
        line-height: 1.4rem;
    }

    .footerContactLink {
        color: #c8c9d0;
        background-color: #111218;
        border: 1px solid #22242f;
        border-radius: 50px;
        justify-content: flex-start;
        align-items: center;
        max-width: 500px;
        min-height: 48px;
        margin-top: 16px;
        margin-bottom: 32px;
        padding: 8px 24px;
        font-size: 12px;
        font-weight: 600;
        line-height: 16px;
        text-decoration: none;
        display: flex;
    }

    .link {
        color: var(--orange);
        text-decoration: none;
    }

    .icon{
        filter: invert();
        width: 24px;
        height: 24px;
        margin-right: 10px;
    }

</style>
