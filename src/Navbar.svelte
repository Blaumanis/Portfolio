<script>
  import {slide} from 'svelte/transition';
  import MobileMenu from './MobileMenu.svelte'
  let open = false;
  window.addEventListener('scroll', fixNav)

function fixNav() {
    const nav = document.querySelector('.navbar')
    if(window.scrollY > nav.offsetHeight) {
        nav.style.backgroundColor = "#fff"
    } else {
        nav.style.backgroundColor = "#fffaeb"
    }
}

function showMobileMenu() {
    open = true;
  }

</script>

<style>
.navbar {
    display: flex;
    justify-content: space-around;
    align-items: center;
    flex-direction: row;
    gap: 0;
    padding: 1.5rem 1rem;
    background-color: var(--pale);
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    z-index: 1000;
}

.logo {
  font-size: 2rem;
  letter-spacing: .5rem;
  text-shadow: 2px 2px 4px var(--black);
}

.logo span {
  color: var(--paleGold);
  text-shadow: 2px 2px 4px var(--paleGold);
}

.links-container {
    display: flex;
    justify-content: space-around;
    align-items: center;
    flex-direction: row;
     gap: 2rem;
}

.link {
  color: var(--darkBlue);
  font-size: 1.25rem;
  font-family: var(--OpenSans);
  transition: var(--trans);
  letter-spacing: 0.25rem;
}

.link:hover {
  color: var(--paleGold);
}

.hamburger-btn {
  display: none;
  border: none;
  background-color: var(--pale);
}

.hamburger-btn i {
  font-size: 2.5rem;
  color: var(--paleGold);
  cursor: pointer;
}
@media (max-width: 768px) {
  .navbar {
    background-color: #fff;
    justify-content: space-between;
  }
  .links-container {
    display: none;
  }
  .hamburger-btn {
    display: block !important;
  }
}

</style>

{#if open}
  <MobileMenu {open}/>
{:else}
  <nav class="navbar" transition:slide>
    <h2 class="logo">Blau<span>Man</span></h2>
    <ul class="links-container">
        <li class="link-li"><a class="link" href="/">Home</a></li>
        <li class="link-li"><a class="link" href="/">About</a></li>
        <li class="link-li"><a class="link" href="/">Projects</a></li>
        <li class="link-li"><a class="link" href="/">Contact</a></li>
    </ul>
    <button class="hamburger-btn" on:click={showMobileMenu}><i class="fa fa-bars"></i></button>
  </nav>
{/if}

