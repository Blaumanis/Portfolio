<script>

</script>

<style>

    .timeline-section {
        padding: 3rem 1rem;
    }

    h2{
        position: relative;
        text-align: center;
        margin-bottom: 5rem;
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

    p {
        margin: 1rem 0;
        padding-left: 1rem;
        padding-right: 1rem;
    }

    h3 {
        padding-left: 1rem;
    }

    .timeline-container {
        display: grid;
        place-items: center;
    }

    .timeline {
        width: 600px;
        padding: 3rem 2rem; 
        position: relative;
        border-top: 2px dashed var(--paleGold);
    }
    .timeline:first-child {
        border-top: 0;
        border-top-right-radius: 0;
    }
    .timeline:nth-child(odd) {
        border-right: 2px dashed var(--paleGold);
        border-bottom-right-radius: var(--borderRadius);
        border-top-right-radius: var(--borderRadius);
        margin-left: var(--borderRadius);
    }
    .timeline:nth-child(even) {
        border-left: 2px dashed var(--paleGold);
        border-top-left-radius: var(--borderRadius);
        border-bottom-left-radius: var(--borderRadius);
        margin-right: var(--borderRadius);
    }

    .timeline:last-child {
        border-bottom-left-radius: 0;
    }

    span {
        position: absolute;
        top: 50%;
        right: -15px;
        transform: translateY(-50%);
        padding: .45rem .75rem;
        background-color: var(--paleGold);
        color: var(--darkBlue);
        border-radius: 50%;
    }
    .timeline:nth-child(even) span {
        left: -15px;
        right: inherit;
    }

    @media (max-width: 768px) {
        .timeline {
            width: 100%;
            padding: 1.5rem 1rem;
        }
    }

</style>

<section class="timeline-section">
    <h2>timeline</h2>
    <article class="timeline-container">
        <div class="timeline">
            <h3>2020</h3>
            <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Id iure voluptatem omnis sequi dolor numquam ipsa nemo suscipit, reprehenderit incidunt.</p>
            <span>1</span>
        </div>
        <div class="timeline">
            <h3>2019</h3>
            <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Id iure voluptatem omnis sequi dolor numquam ipsa nemo suscipit, reprehenderit incidunt.</p>
            <span>2</span>
        </div>
        <div class="timeline">
            <h3>2018</h3>
            <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Id iure voluptatem omnis sequi dolor numquam ipsa nemo suscipit, reprehenderit incidunt.</p>
            <span>3</span>
        </div>
        <div class="timeline">
            <h3>2017</h3>
            <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Id iure voluptatem omnis sequi dolor numquam ipsa nemo suscipit, reprehenderit incidunt.</p>
            <span>4</span>
        </div>
        <div class="timeline">
            <h3>2016</h3>
            <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Id iure voluptatem omnis sequi dolor numquam ipsa nemo suscipit, reprehenderit incidunt.</p>
            <span>5</span>
        </div>
        <div class="timeline">
            <h3>2015</h3>
            <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Id iure voluptatem omnis sequi dolor numquam ipsa nemo suscipit, reprehenderit incidunt.</p>
            <span>6</span>
        </div>
    </article>
</section>

