<script>

</script>

<style>
    .about {
        display: flex;
        justify-content: space-around;
        align-items: flex-start;
        padding: 4rem 1rem;
    }

    .img-container {
        flex-basis: 40%;
        display: flex;
        justify-content: center;
        position: relative;
    }

    .box {
        height: 450px;
        left: 65px;
    }

    .content {
        flex-basis: 60%;
    }

    h2 {
        position: relative;
    }

    h2::before {
        content: '';
        width: 93px;
        height: 4px;
        position: absolute;
        bottom: -20px;
        background-color: var(--paleGold);
    }

    .first-paragraph {
        margin: 3rem 0 1rem 0;
    }

    button {
        margin-top: 2rem;
    }

    @media (max-width: 1000px) {
        .about {
            flex-direction: column;
            align-items: center;
        }

        .img-container {
            margin-bottom: 3rem
        }

        .box {
            display: none;
        }
    }

    @media (max-width: 500px) {
        img {
            width: 100%;
        }
    }

</style>

<section class="about">
    <article class="img-container">
        <div class="box"></div>
        <img class="hero-img" src="/images/about-img.jpeg" alt="girl-with-camera">
    </article>
    <article class="content">
        <h2>About</h2>
        <p class="first-paragraph">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Debitis, inventore quaerat iste labore pariatur rerum dolor natus ipsum ipsam est minus earum laudantium aperiam omnis nisi? Harum, numquam architecto consequatur sequi, at quasi eveniet tempora eligendi sit nostrum vel eius corrupti reiciendis atque voluptas!</p>
        <p class="second paragraph">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Debitis, inventore quaerat iste labore pariatur rerum dolor natus ipsum ipsam est minus earum laudantium aperiam omnis nisi? Harum, numquam architecto consequatur sequi, at quasi eveniet tempora eligendi sit nostrum vel eius corrupti reiciendis atque voluptas!</p>
        <button class="btn-primary">about me</button>
    </article>
</section>