<script>
    import {fade} from 'svelte/transition';
    import ContactForm from './ContactForm.svelte'
    let openForm = false;

    function isFormOpen() {
        openForm = true;
    }

</script>

<style>
    .main-container {
        position: relative;
        height: 100vh;
        width: 100vw;
        margin-bottom: 5rem;
        clip-path: polygon(50% 0, 100% 10%, 100% 90%, 50% 100%, 0 90%, 0 10%);
    }

    .modal {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        width: 500px;
        background-color: var(--pale);
        text-align: center;
        padding: 2rem;
    }

    h2 {
        position: relative;
        margin: 1rem 0 3rem
    }

    h2::before {
        content: '';
        width: 93px;
        height: 4px;
        position: absolute;
        bottom: -15px;
        left: 50%;
        transform: translateX(-50%);
        background-color: var(--paleGold);
    }

    button {
        margin: 1.5rem auto;
    }

    video {
        position: absolute;
        width: 100%;
        height: 100%;
        opacity: 0.5;
        object-fit: cover;
        top: 0;
        left: 0;
    }

    @media (max-width: 768px) {
        .modal {
            width: 100%;
        }
    }

</style>

<section class="main-container">
{#if openForm}
    <ContactForm {openForm}/>
{:else}
        <video src="/images/connect.mp4" autoplay muted loop poster="poster-img.avif" transition:fade></video>
        <article class="modal">
            <h2>let's get in touch</h2>
            <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Quos possimus quaerat praesentium repellat ipsum? Vitae soluta eum numquam doloremque maiores dolores expedita recusandae voluptatibus, eveniet perspiciatis, odit adipisci fugit incidunt aliquam omnis facilis nam?</p>
            <button class="btn-primary" on:click={isFormOpen}>contact me</button>
        </article>
{/if}
</section>
