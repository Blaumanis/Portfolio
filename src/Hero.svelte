<script>
    import Navbar from './Navbar.svelte'
</script>

<style>
    .hero {
        height: 100vh;
        background-color: var(--pale);
        display: flex;
        justify-content: space-evenly;
        align-items: center;
        gap: 1rem;
        padding: 0 1rem;
    }

    .content {
        display: flex;
        flex-direction: column;
        gap: 1rem;
        padding-right: 1rem;
        padding-top: 2rem;
    }

    .photo {
        position: relative;
        padding-top: 4rem;
    }

    h1 {
        font-size: 4rem;
    }

    h1::before {
        content: '';
        width: 93px;
        height: 4px;
        position: absolute;
        top: -20px;
        background-color: var(--paleGold);
    }

    p {
        font-size: 1.15rem;
        font-weight: 700;
        letter-spacing: 0.15rem;
    }

    .social-icons {
        display: flex;
        justify-content: flex-start;
        gap: 2rem;
        align-items: center;
    }

    .social-icons i {
        font-size: 1.5rem;
        color: var(--darkBlue);
        transition: var(--trans);
    }

    .social-icons i:hover {
        color: var(--paleGold);
    }

    @media (max-width: 768px) {
        .photo {
            display: none;
        }
    }

</style>
<Navbar />
<main class="hero">
    <section class="content">
        <h1>I'm Alberts</h1>
        <p>Freelance Web & Mobile UI/UX Designer</p>
        <button class="btn-primary">hire me</button>
        <div class="social-icons">
            <a href="/"><i class="fab fa-linkedin"></i></a>
            <a href="/"><i class="fab fa-github"></i></a>
            <a href="/"><i class="fab fa-twitter"></i></a>
            <a href="/"><i class="fab fa-instagram"></i></a>
        </div>
    </section>
    <section class="photo">
        <div class="box"></div>
        <img class="hero-img" src="images/main-photo.jpg" alt="man">
    </section>
</main>