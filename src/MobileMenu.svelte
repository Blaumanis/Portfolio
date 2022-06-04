<script>
import {slide} from 'svelte/transition';
import Navbar from './Navbar.svelte'
export let open;

function hideMobileMenu() {
    open = false;
  }
</script>

<style>

    .mobile-menu {
        height: 100vh;
        width: 100vw;
        background-color: var(--lightGray);
        display: flex;
        flex-direction: column;
        gap: 4rem;
        align-items: center;
        justify-content: center;
        position: fixed;
        top: 0;
        left: 0;
        z-index: 10000;
    }

    .links-container {
        display: flex;
        flex-direction: column;
        gap: 2rem;
        align-items: center;
        justify-content: center;
    }

    .link {
        color: var(--lightBlue);
        font-size: 2rem;
        font-family: var(--OpenSans);
        transition: var(--trans);
    }

    .link:hover {
        color: var(--paleGold);
    }

    .social-icons {
        display: flex;
        align-items: center;
        justify-content: space-around;
        gap: 3rem;
    }

    .social-icons i {
        font-size: 1.5rem;
        color: var(--darkBlue);
        transition: var(--trans);
    }

    .social-icons i:hover {
        color: var(--paleGold);
    }

    button {
        border: none;
        background-color: var(--lightGray);
        cursor: pointer;
    }

    .close {
        position: absolute;
        top: 1rem;
        right: 2rem;
        font-size: 3rem;
        color: var(--tomato);
        transition: var(--trans);
    }

    .close:hover {
        transform: rotate(180deg);
    }


</style>
{#if open}
<section class="mobile-menu" transition:slide>
    <ul class="links-container">
        <li class="link-li"><a class="link" href="/">Home</a></li>
        <li class="link-li"><a class="link" href="/">About</a></li>
        <li class="link-li"><a class="link" href="/">Projects</a></li>
        <li class="link-li"><a class="link" href="/">Contact</a></li>
    </ul>
    <div class="social-icons">
        <a href="/"><i class="fab fa-linkedin"></i></a>
        <a href="/"><i class="fab fa-github"></i></a>
        <a href="/"><i class="fab fa-twitter"></i></a>
        <a href="/"><i class="fab fa-instagram"></i></a>
    </div>
    <button on:click={hideMobileMenu}><i class="fas fa-times close"></i></button>
</section>
{:else}
    <Navbar />
{/if}