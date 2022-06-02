<script>

</script>

<style>

    .blog-section {
        padding: 2rem;
        background-color: var(--lightGray);
    }

    h2 {
        position: relative;
        margin: 3rem 0;
        text-align: center;
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

    .blog-container {
        /* display: flex;
        flex-wrap: wrap;
        justify-content: space-around;
        align-items: center; */
        display: grid;
        grid-template-columns: 1fr 1fr;
        grid-template-rows: 1fr 1fr;
        justify-items: center;
        gap: 2rem;
        padding: 3rem 0;
    }

    /* individual card */
    .card {
        background-color: transparent;
        width: 80%;
        height: 400px;
        border-radius: var(--borderRadius);
        transition: all 2s linear;
        perspective: 1000px;
    }

    .card-inner {
        position: relative;
        width: 100%;
        height: 100%;
        transition: all 2s linear;
        transform-style: preserve-3d;
    }

    .card:hover .card-inner {
         transform: rotateY(180deg);
    }

    .card-front, .card-back {
        position: absolute;
        width: 100%;
        height: 100%;
        -webkit-backface-visibility: hidden;
        backface-visibility: hidden;
    }

    /* card front */
    .card-front {
        display: flex;
        flex-direction: column;
        gap: 1rem;
        border-radius: var(--borderRadius);
        background-color: #fff;
        overflow: hidden;
    }

    .card-img {
        display: block;
        width: 100%;
        max-height: 200px;
        aspect-ratio: 16 / 9;
        object-fit: cover;
        object-position: center;
    }

    h3, p, .card-footer {
        padding: 0 1rem;
    }

    .card-footer {
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    span {
        text-transform: uppercase;
        color: var(--paleGold);
    }

    .thumbnail {
        width: 40px;
        height: 40px;
        border-radius: 100%;
        aspect-ratio: 16 / 9;
        object-fit: cover;
        object-position: center;
    }

    /* card back */
    .card-back {
        background-color: var(--pale);
        display: grid;
        place-items: center;
        transform: rotateY(180deg);
        border-radius: var(--borderRadius);
    }

    @media (max-width: 950px){
        .blog-container {
            grid-template-columns: 1fr;
            grid-template-rows: auto;
        }

        .card {
            width: 100%;
        }
    }


</style>

<section class="blog-section">
    <h2>Blog</h2>

    <article class="blog-container">

        <div class="card">
            <div class="card-inner">
              <div class="card-front">
                <img src="/images/project-1.jpeg" alt="project-4" class="card-img">
                <h3>article title</h3>
                <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Nesciunt numquam cum laudantium veniam voluptate ad veritatis, vitae officia voluptatem amet.</p>
                <div class="card-footer">
                    <img src="/images/hero-img-small.jpeg" alt="thumbnail" class="thumbnail">
                    <span>7 min read</span>
                </div>
              </div>
              <div class="card-back">
                <button class="btn-primary">read more</button>
              </div>
            </div>
          </div>

          <div class="card">
            <div class="card-inner">
              <div class="card-front">
                <img src="/images/project-2.jpeg" alt="project-4" class="card-img">
                <h3>article title</h3>
                <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Nesciunt numquam cum laudantium veniam voluptate ad veritatis, vitae officia voluptatem amet.</p>
                <div class="card-footer">
                    <img src="/images/hero-img-small.jpeg" alt="thumbnail" class="thumbnail">
                    <span>7 min read</span>
                </div>
              </div>
              <div class="card-back">
                <button class="btn-primary">read more</button>
              </div>
            </div>
          </div>

          <div class="card">
            <div class="card-inner">
              <div class="card-front">
                <img src="/images/project-3.jpeg" alt="project-4" class="card-img">
                <h3>article title</h3>
                <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Nesciunt numquam cum laudantium veniam voluptate ad veritatis, vitae officia voluptatem amet.</p>
                <div class="card-footer">
                    <img src="/images/hero-img-small.jpeg" alt="thumbnail" class="thumbnail">
                    <span>7 min read</span>
                </div>
              </div>
              <div class="card-back">
                <button class="btn-primary">read more</button>
              </div>
            </div>
          </div>

          <div class="card">
            <div class="card-inner">
              <div class="card-front">
                <img src="/images/project-4.jpeg" alt="project-4" class="card-img">
                <h3>article title</h3>
                <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Nesciunt numquam cum laudantium veniam voluptate ad veritatis, vitae officia voluptatem amet.</p>
                <div class="card-footer">
                    <img src="/images/hero-img-small.jpeg" alt="thumbnail" class="thumbnail">
                    <span>7 min read</span>
                </div>
              </div>
              <div class="card-back">
                <button class="btn-primary">read more</button>
              </div>
            </div>
          </div>

    </article>

</section>