<template>
  <section id="portfolio">
        <h1>My Work</h1>
        <article class="work-list">
            <figure class="work">
                <img :src="fPortfolioWork" />
                <figcaption class="text">
                    <h3>Work & Study Website</h3>
                    <p>Discover opportunities for work and study in Canada, your gateway to success.</p>
                    <!-- <p>Discover boundless work and study chances in Canada, your gateway to success.</p> -->
                    <a href="https://github.com/santiagorave/FinalProject.git" target="blank"><i class="fa-solid fa-up-right-from-square"></i></a>
                </figcaption>
            </figure>
            <figure class="work">
                <img :src="sPortfolioWork" />
                <figcaption class="text">
                    <h3>Library Management System App</h3>
                    <!-- <p>Efficiently manage library resources and book study rooms with the comprehensive library management system.</p> -->
                    <p>Efficiently manage library resources, book study rooms, and enjoy comprehensive system.</p>
                    <a href="https://github.com/riki-nakayashiki/LibraWeb.git" target="blank"><i class="fa-solid fa-up-right-from-square"></i></a>
                </figcaption>
            </figure>
            <figure class="work">
                <img :src="tPortfolioWork" />
                <figcaption class="text">
                    <h3>Jewelry E-shop App</h3>
                    <!-- <p>Explore a stunning collection of jewelry and indulge in the elegance of the virtual boutique.</p> -->
                    <p>Discover boundless work and study chances in Canada, your gateway to unparalleled success.</p>
                    <a href="https://github.com/kimhyerim511/final-jewelrylane.git" target="blank"><i class="fa-solid fa-up-right-from-square"></i></a>
                </figcaption>
            </figure>
        </article>
  </section>
</template>

<script>
import fPortfolioWork from "../../img/work-6.png";
import sPortfolioWork from "../../img/work-2.png";
import tPortfolioWork from "../../img/work-3.png";

export default {
    name: "PortfolioSection",
    data() {
        return {
            fPortfolioWork: fPortfolioWork,
            sPortfolioWork: sPortfolioWork,
            tPortfolioWork: tPortfolioWork,
        }
    }
}
</script>

<style>
    #portfolio {
        padding: 30px 0;
    }

    #portfolio h1 {
        color: #355070;
        padding-left: 10%;
        /* padding-top: 3%; */
        font-size: 35px;
        font-weight: 600;
    }
    .work-list {
        display: flex;
        column-gap: 5vh;
        padding: 2% 80px 0 10%;
    }

    .work {
        border-radius: 10px;
        position: relative;
        overflow: hidden;
    }

    .work img {
        width: 100%;
        border-radius: 10px;
        display: block;
        transition: 0.5s;
    }

    .text {
        width: 100%;
        height: 0%;
        border-radius: 10px;
        position: absolute;
        left: 0;
        bottom: 0;
        overflow: hidden;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        text-align: center;
        padding: 0px 40px;
        font-size: 14px;
        background: linear-gradient(rgba(0, 0, 0, 0.6), #d98e8e);
        color: whitesmoke;
        row-gap: 2vh;
        transition: 0.5s;
    }

    .text h3 {
        font-weight: 500;
    }

    .text a {
        /* padding-top: 20px; */
        text-decoration: none;
        font-size: 18px;
        background: #fff;
        width: 50px;
        height: 50px;
        border-radius: 50%;
        text-align: center;
        display: flex;
        justify-content: center;
        align-content: center;
        color: #355070;
        /* color: #d98e8e; */
        color: #8d5954;
        /* color: #dd6e6e; */
    }

    .text i {
        display: flex;
        align-items: center;
    }

    .work:hover img {
        transform: scale(1.1);
    }

    .work:hover .text {
        height: 100%;
    }

    /***** DARK MODE *****/
    .dark-mode #portfolio h1 {
        color: #4e75a5;
    }
</style>