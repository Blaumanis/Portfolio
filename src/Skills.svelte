<script>

</script>

<style>

.skills-section {
    background-color: var(--beige);
    padding: 3rem 1rem;
}

h2 {
    text-align: center;
    margin-bottom: 4rem;
}

h2::before {
    content: '';
    width: 93px;
    height: 4px;
    position: absolute;
    bottom: -20px;
    left: 50%;
    transform: translateX(-50%);
    background-color: var(--paleGold)   
}

.skills-container {
    display: grid;
    grid-template-columns: 1fr 1fr;
    justify-items: center;
    gap: 1rem;
    padding: 0 1rem;
}

h3 {
    font-size: 1.5rem;
    color: var(--brown);
    margin-bottom: 2rem;
}

p {
    color: var(--brown);
}

.front-end, .back-end {
    width: 80%;
}

.skill {
    height: 20px;
    background-color: var(--paleGold);
    border-radius: var(--borderRadius);
    margin: 3rem 0;
    position: relative;
}

.skill::before {
    content: '';
    position: absolute;
    top: 0;
    right: 0;
    width: 50%;
    height: 100%;
    background-color: #fff;
    border-top-right-radius: var(--borderRadius);
    border-bottom-right-radius: var(--borderRadius);
}

.seventy::before{
    width: 30% !important;
}

.eighty::before{
    width: 20% !important;
}

.skill-name {
    position: absolute;
    top: -25px;
}

.skill-percentage {
    position: absolute;
    top: -25px;
    left: 50%;
    transform: translateX(-50%);
}

.seventy .skill-percentage{
    left: 70%;
    transform: translateX(-70%);
}

.eighty .skill-percentage{
    left: 80%;
    transform: translateX(-80%);
}

@media (max-width: 768px) {
    .skills-container {
        grid-template-columns: 1fr;
        grid-template-rows: 1fr 1fr;
    }

    .front-end, .back-end {
        width: 100%;
    }
}

</style>

<section class="skills-section">
    <h2>Skills</h2>
    <article class="skills-container">
        <div class="front-end">
            <h3>front end</h3>
            <div class="skill">
                <p class="skill-name">HTML/CSS</p>
                <p class="skill-percentage">50%</p>
            </div>
            <div class="skill seventy">
                <p class="skill-name">Javascript</p>
                <p class="skill-percentage">70%</p>
            </div>
            <div class="skill eighty">
                <p class="skill-name">Svelte</p>
                <p class="skill-percentage">80%</p>
            </div>
        </div>
        <div class="back-end">
            <h3>back end</h3>
            <div class="skill">
                <p class="skill-name">Node</p>
                <p class="skill-percentage">50%</p>
            </div>
            <div class="skill seventy">
                <p class="skill-name">PHP</p>
                <p class="skill-percentage">70%</p>
            </div>  
            <div class="skill eighty">
                <p class="skill-name">Python</p>
                <p class="skill-percentage">80%</p>
            </div>
        </div>
    </article>
</section>