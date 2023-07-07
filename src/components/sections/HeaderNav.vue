<template>
        <!-- NAVIGATION MENU -->
        <DarkModeButton/>
        <nav>
            <figure class="nav-menu">
                <img :src="logoSrc">
                <ul>
                    <li>
                        <a href="#home">Home</a>
                    </li>
                    <li>
                        <a href="#about">About</a>
                    </li>
                    <li>
                        <a href="#services">Services</a>
                    </li>
                    <li>
                        <a href="#portfolio">Portfolio</a>
                    </li>
                    <li>
                        <a href="#contact">Contact</a>
                    </li>
                </ul>
            </figure>
        </nav>
        <!-- NAVIGATION MENU END -->
</template>

<script>
import myLogo from '../../img/logo.png'
import DarkModeButton from './DarkModeButton.vue'
export default {
    name: "HeaderNav",
    components: {
        DarkModeButton
    },
    props: {
    darkMode: Boolean
    },
    data() {
        return {
            logoSrc: myLogo,
            // logoSrcDark: myLogoDark,
        }
    },
//     computed: {
//     logoSrc() {
//       return this.darkMode ? this.logoSrcDark : this.logoSrcLight;
//     }
//   },
}
</script>

<style>
    /* .dark-mode {
    background-image: url('../../img/logo-dark.png');
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    } */

    nav img {
        width: 30%;
    }

    nav {
        padding: 10px 10%;
    }

    nav figure {
        display: flex;
        align-items: center;
        justify-content: space-between;
        flex-wrap: wrap;
    }

    .nav-menu ul {
        display: flex;
        width: 50%;
        list-style: none;
    }

    .nav-menu li {
        text-align: center;
        width: 100%;
    }

    .nav-menu a {
        color: #355070;
        text-decoration: none;
        font-size: 18px;
        cursor: pointer;
        position: relative;
    }

    .nav-menu a::after {
        content: '';
        width: 0;
        height: 3px;
        background: #8d5954;
        background: #dd6e6e;
        position: absolute;
        left: 0;
        bottom: -6px;
        transition: 0.4s;
    }

    .nav-menu a:hover::after {
        width: 100%;
    }


    /***** DARK MODE *****/
    .dark-mode .nav-menu a {
        color:#dd6e6e;
        color:#4e75a5;
    }
</style>