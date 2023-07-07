<template>
    <section id="contact">
            <section class="row">
                <article class="left">
                    <h1>Contact Me</h1>
                    <p><i class="fa-solid fa-paper-plane"></i>moncanem@gmail.com </p>
                    <p><i class="fa-solid fa-phone"></i>+1 (236) 688-3034</p>
                    <section class="icons">
                        <a href="https://www.linkedin.com/in/monika-nemcov%C3%A1-17778320b/" target="blank"><i class="fa-brands fa-linkedin"></i></a>
                        <a href="https://www.instagram.com/moncanem/" target="blank"><i class="fa-brands fa-instagram"></i></a>
                        <a href="https://github.com/moncanem" target="blank"><i class="fa-brands fa-github"></i></a>
                    </section>
                    <a href="/Monika Nemcova - resume.pdf" download class="cv">Download Cv</a>
                </article>
                <article class="right">
                    <form name="submit-to-google-sheet">
                        <input type="text" name="name" placeholder="Your Name" required>
                        <input type="email" name="email" placeholder="Your Email" required>
                        <textarea name="message" rows="6" placeholder="Your Message"></textarea>
                        <button class="submit" type="submit" @click.prevent="submitForm">Submit</button>
                    </form>
                </article>
            </section>
        </section>
</template>

<script>
export default {
    name: "ContactSection",
//     methods: {
//     submitForm() {
//       const scriptURL = 'https://script.google.com/macros/s/AKfycbzzRjkA4mrN_5FXj349bqDZT9pBHabgIoftWPjAJuhfLYJZ7HBbi7GhVz7U_riYnbmK/exec';
//       const form = this.$refs.contactForm;

//       fetch(scriptURL, {
//         method: 'POST',
//         body: new FormData(form),
//       })
//         .then(response => {
//           console.log('Success!', response);
//           // Handle success response
//         })
//         .catch(error => {
//           console.error('Error!', error.message);
//           // Handle error
//         });
//     },
//   },
}
</script>

<style>

    #contact {
        padding-top: 50px;
    }

    .left {
        flex-basis: 35%;
        padding-left: 10%;
    }

    .left h1 {
        color: #355070;
        /* padding-top: 3%; */
        font-size: 35px;
        font-weight: 600;
    }

    .left p {
        padding-top: 30px;
        color: #355070;
        transition: 0.5s;
        cursor: pointer;
    }

    .left i {
        color:#355070;
        padding-right: 15px;
        font-size: 20px;
    }

    .right {
        flex-basis: 60%;
    }

    .icons {
        padding-top: 30px;
        padding-bottom: 30px;
    }

    .icons a {
        text-decoration: none;
        padding-right: 15px;
        color: #355070;
        display: inline-block;
    }

    .icons i {
        font-size: 30px;
        transition: 0.5s;
    }

    .icons i:hover,
    .left p:hover {
        color: #d98e8e;
        transform: translateY(-5px);
    }

    .cv {
        text-decoration: none;
        background-color:#d98e8e;
        color: #355070;
        padding: 3%;
        border: 2.5px solid #d98e8e;
        border-radius: 10px;
        transition: 0.5s;
        font-weight: 400;
    }

    .cv:hover,
    .submit:hover {
        background-color: #F6F4F1;
        color: #d98e8e;
    }

    .submit {
        background-color:#d98e8e;
        color: #355070;
        padding: 1.5%;
        border: 2.5px solid #d98e8e;
        border-radius: 10px;
        transition: 0.5s;
        width: 15%;
        font-weight: 400;
        font-size: 16px;
        cursor: pointer;
    }

    .right form {
        width: 95%;
        display: flex;
        flex-direction: column;
        row-gap: 2vh;
        align-items: center;
    }

    .right input,
    .right textarea {
        width: 100%;
        border: 0;
        outline: none;
        background-color: white;
        color: #355070;
        padding: 15px;
        font-size: 16px;
        border-radius: 6px;
        resize: none;
    }


    /***** DARK MODE *****/
    .dark-mode .left h1,
    .dark-mode .left p,
    .dark-mode .left i {
        color: #4e75a5;
    }

    .dark-mode .icons i:hover,
    .dark-mode .left p:hover {
        color: #d98e8e;
        transform: translateY(-5px);
    }

    .dark-mode input,
    .dark-mode textarea {
        background-color: gainsboro;
    }

    .dark-mode .cv:hover,
    .dark-mode .submit:hover {
        background-color: gainsboro;
    }
</style>