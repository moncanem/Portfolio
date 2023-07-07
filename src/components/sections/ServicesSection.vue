<template>
  <!-- SERVICES SECTION -->
  <section id="services">
        <h1>My Services</h1>
        <article class="services-list">
            <article>
                <h2>Web Design and Development</h2>
                <p>
                I transform ideas into stunning websites, specializing in visually
                captivating online experiences. With expertise in HTML, CSS,
                JavaScript, and proficiency in WordPress and Bootstrap, I create
                functional websites that impress.
                </p>
            </article>
            <article>
                <h2>Responsive Web Design</h2>
                <p>
                I excel in crafting adaptive websites, ensuring exceptional
                experiences across devices. Using cutting-edge techniques and
                responsive design principles, I guarantee flawless functionality and
                exceptional visuals on desktops, tablets, and mobile devices.
                </p>
            </article>
            <article>
                <h2>Custom Web Development</h2>
                <p>
                With a deep understanding of client needs, I create tailored web
                solutions. From database integration to complex functionality, I
                deliver customized, purpose-built applications that empower businesses
                and enhance user experiences.
                </p>
            </article>
        </article>
  </section>
  <!-- SERVICES SECTION END -->
</template>

<script>
export default {
  name: "ServicesSection",
};
</script>

<style>
    #services {
    padding: 30px 0;
    color: #355070;
    }

    #services h1 {
    padding-left: 10%;
    padding-top: 3%;
    font-size: 35px;
    font-weight: 600;
    }

    /* .services-list {
            display: grid;
            grid-template-columns: repeat(auto-fit,minmax(250px,1fr));
            grid-gap: 40px;
            padding-top: 50px;
        } */

    .services-list {
    display: flex;
    padding-left: 10%;
    padding-top: 2%;
    column-gap: 5vh;
    }

    .services-list article {
    width: 29%;
    text-align: justify;
    background-color: #d98e8e;
    padding: 1%;
    height: 25vh;
    border-radius: 10px;
    transition: 0.5s;
    /* color: whitesmoke; */
    }

    .services-list article:hover {
    background-color: #dd6e6e;
    transform: translateY(-10px);
    }

    .services-list p {
    line-height: 1.5;
    }


    /***** DARK MODE *****/
    .dark-mode #services h1 {
        color: #4e75a5;
    }

    .dark-mode .services-list article {
        background-color: rgb(179, 179, 179);
    }

    .dark-mode .services-list article:hover {
    background-color:#d98e8e;
    transform: translateY(-10px);
    }
</style>