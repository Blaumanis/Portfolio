<script>

</script>

<style>
    .service-container {
        background-color: var(--lightGray);
        padding: 2rem;
    }

    h2 {
        text-align: center;
        position: relative;
        margin-bottom: 2rem;
    }

    h2::before {
        content: '';
        width: 93px;
        height: 4px;
        position: absolute;
        bottom: -20px;
        left: 50%;
        transform: translateX(-50%);
        background-color: var(--paleGold);
    }


    .service-content {
        padding: 2rem 0;
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 2rem;
        text-align: center;
    }

    .service-box {
        background-color: #fff;
        border-radius: var(--borderRadius);
        padding: 1rem;
        display: flex;
        flex-direction: column;
        gap: 1rem;
        transition: var(--trans);
    }

    .service-box:hover {
        background-color: var(--paleGold);
    }

    .service-box:hover > i, .service-box:hover > h3, .service-box:hover > p {
        color: #fff;
    }
    
    
    i {
        font-size: 2rem;
        color: var(--darkBlue);
        transition: var(--trans);
    }

    h3 {
        font-size: 1rem !important;
        text-transform: capitalize;
        margin-bottom: 1rem;
        transition: var(--trans);
    }

    h3::after {
        content: '';
        width: 40px;
        height: 3px;
        position: absolute;
        bottom: -15px;
        left: 50%;
        transform: translateX(-50%);
        background-color: var(--paleGold);
    }

    p {
        transition: var(--trans);
    }

    @media (max-width: 1000px) {
        .service-content {
            grid-template-columns: 1fr 1fr;
        }
        
        .service-box:nth-child(3) {
            grid-column: 1/3;
        }
    }

    @media (max-width: 620px) {
        .service-content {
            grid-template-columns: 1fr;
            grid-template-rows: repeat(3, 1fr);
        }
        
        .service-box:nth-child(3) {
            grid-column: 1/2
        }
    }

</style>

<section class="service-container">
    <h2>Services</h2>
    <article class="service-content">
        <div class="service-box">
            <i class="fas fa-code service-icon"></i>
            <h3>web development</h3>
            <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Illum ea nesciunt corrupti voluptate debitis? Natus iusto veniam illum dolores molestias.</p>
        </div>
        <div class="service-box">
            <i class="fab fa-sketch service-icon"></i>
            <h3>web design</h3>
            <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Illum ea nesciunt corrupti voluptate debitis? Natus iusto veniam illum dolores molestias.</p>
        </div>
        <div class="service-box">
            <i class="fab fa-android service-icon"></i>
            <h3>app design</h3>
            <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Illum ea nesciunt corrupti voluptate debitis? Natus iusto veniam illum dolores molestias.</p>
        </div>
    </article>
</section>