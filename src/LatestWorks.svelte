<script>

</script>

<style>
    .latest-works {
        padding: 5rem 1rem;
        text-align: center;
    }

    .info {
        width: 400px;
        margin: 0 auto 3rem;
    }

    h2 {
        margin-bottom: 3rem;
    }

    h2::after {
        content: '';
        width: 93px;
        height: 4px;
        position: absolute;
        bottom: -20px;
        left: 50%;
        transform: translateX(-50%);
        background-color: var(--paleGold);
    }

    .work-examples {
        display: grid;
        grid-template-areas: 
            "a b b"
            "a c d";
        grid-template-columns: 1fr 1fr 1fr;
        grid-template-rows: 200px 200px;
        gap: 1rem;
        max-width: 1000px;
        min-width: 80%;
        margin: 0 auto;
    }

    .work {
        border-radius: var(--borderRadius);
        background-position: center;
        background-repeat: no-repeat;
        background-size: cover;
        position: relative;
        transition: var(--trans);
    }

    .work::before {
        content: '';
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        opacity: 0;
        background-color: var(--paleGold);
        transition: var(--trans);
    }

    .work::after{
        content: '';
        position: absolute;
        width: 100%;
        height: 100%;
        top: 0;
        left: 0;
        border: 3px solid #fff;
        border-radius: var(--borderRadius);
        opacity: 0;
        transition: var(--trans);
    }

    .work:hover::before {
        opacity: 0.5;
    }

    .work:hover::after {
        opacity: 1;
        transform: scale(0.8);
    }

    .work:hover > .work-info {
        opacity: 1;
    }

    .first-work {
        grid-area: a;
        background-image: url('/images/project-1.jpeg');
    }

    .second-work {
        grid-area: b;
        background-image: url('/images/project-2.jpeg');
    }

    .third-work {
        grid-area: c;
        background-image: url('/images/project-3.jpeg');
    }

    .fourth-work {
        grid-area: d;
        background-image: url('/images/project-4.jpeg');
    }

    .work-info {
        position: absolute;
        width: 100%;
        height: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        gap: 1rem;
        opacity: 0;
        transition: var(--trans);
        z-index: 1000;
    }

    .work-info h3, .work-info h4 {
        color: #fff;
        text-align: center;
    }

    @media (max-width: 1000px) {
        .work-examples {
        grid-template-areas: 
            "a b "
            "c d";
        grid-template-columns: 1fr 1fr;
        width: 100%;
        }
    }

    @media (max-width: 620px) {
        .work-examples {
        grid-template-areas: 
            "a"
            "b"
            "c"
            "d";
        grid-template-columns: 1fr;
        grid-template-rows: repeat(4, 200px);
        }
        .info {
            width: 100%;
        }
    }



</style>

<section class="latest-works">
    <article class="info">
        <h2>latest works</h2>
        <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Odio eligendi maxime repellat earum, facere nulla ipsa numquam, eos non repellendus quae, tenetur error doloribus eveniet. Ipsa blanditiis, explicabo tenetur laudantium ea fugit veritatis qui iure alias fugiat maiores itaque labore?</p>
    </article>
    <article class="work-examples">

        <a class="work first-work" href="/">
           <article class="work-info">
               <h3>project title</h3>
               <h4>client name</h4>
           </article>
        </a>
        <a class="work second-work" href="/">
            <article class="work-info">
                <h3>project title</h3>
                <h4>client name</h4>
            </article>
        </a>
        <a class="work third-work" href="/">
            <article class="work-info">
                <h3>project title</h3>
                <h4>client name</h4>
            </article>
        </a>
        <a class="work fourth-work" href="/">
            <article class="work-info">
                <h3>project title</h3>
                <h4>client name</h4>
            </article>
        </a>

    </article>
</section>