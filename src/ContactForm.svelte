<script>
    import {fade} from 'svelte/transition';
    import GetInTouch from "./GetInTouch.svelte";
    export let openForm;

	function closeForm() {
		openForm = false;
	}

</script>

<style>

    .form-article {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background-color: var(--pale);
        display: grid;
        justify-content: center;
    }

    .contact-form {
        width: 500px;
        padding: 2rem;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        gap: 1rem;
        background-color: var(--lightGray);
        position: relative;
    }

    h2 {
        margin-bottom: 2rem;
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

    .input-group {
        display: flex;
        align-items: flex-start;
        justify-content: center;
        flex-direction: column;
        gap: 0.5rem;
        width: 100%;
    }

    label {
        color: var(--darkBlue);
        text-transform: uppercase;
    }

    input, textarea {
        width: 100%;
        padding: 1rem;
        color: var(--darkBlue);
        border: none;
        outline: none;
        border-radius: var(--borderRadius);
        font-size: 1.15rem;
        background: #ecf0f3;
        box-shadow: inset 6px 6px 6px #cbced1, inset -6px -6px 6px white;
        font-family: var(--Roboto);
    }

    input::placeholder, textarea::placeholder {
        color: var(--darkBlue) !important;
        font-family: var(--Roboto) !important;
        font-size: 1.15rem;
    }

    .submit, .close {
        width: 100%;
    }

    .close {
        position: absolute;
        bottom: -32px;
        height: 50px;
        display: flex;
        border-radius: 0;
        align-items: center;
        justify-content: center;
        background-color: var(--tomato);
        color: #fff;
    }

    @media (max-width: 600px) {
        .contact-form {
            width: 100vw;
        }
    }

</style>

<!-- <svelte:window on:click={handleClick}/> -->


{#if openForm}
    <article class="form-article" transition:fade>
        <form class="contact-form">
            <h2>contact us</h2>
            <div class="input-group">
                <label for="name">name</label>
                <input type="text" id="name" placeholder="your name">
            </div>
            <div class="input-group">
                <label for="email">email</label>
                <input type="email" id="email" placeholder="your email">
            </div>
            <div class="input-group">
                <label for="message">leave your message</label>
                <textarea name="message" id="message" cols="20" rows="5" placeholder="your message"></textarea>
            </div>
            <button type="submit" class="btn-primary submit">send</button>
            <div on:click={closeForm} class="btn-primary close">close</div>
        </form>
    </article>
{:else}
    <GetInTouch />
{/if}

