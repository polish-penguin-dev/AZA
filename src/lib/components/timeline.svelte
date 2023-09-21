<script>
    let posts = [
        {
            day: 'Wednesday',
            timestamp: '07-12-22 06:00 GMT',
            articles: [
                {
                    img: 'path/to/your/image.jpg',
                    title: 'Sample Post Title 1',
                    body: 'Description or summary for the post 1.'
                },
                {
                    img: 'path/to/your/image2.jpg',
                    title: 'Sample Post Title 2',
                    body: 'Description or summary for the post 2.'
                }
            ]
        },
        {
            day: 'Thursday',
            timestamp: '08-12-22 08:00 GMT',
            articles: [
                {
                    img: 'path/to/your/image3.jpg',
                    title: 'Sample Post Title 3',
                    body: 'Description or summary for the post 3.'
                }
            ]
        }
    ];
</script>

<div class="timeline">
    {#each posts as post}
        <div class="timeline-item">
            <div class="timeline-item-header">
                <div class="timeline-item-day">
                    <i class="fa-solid fa-circle"></i>
                    <h2>{post.day}</h2>
                </div>
                <h3 class="timeline-item-timestamp">{post.timestamp}</h3>
            </div>
            {#each post.articles as article}
                <div class="timeline-item-article">
                    <img src={article.img} alt={article.title}>
                    <h3 class="timeline-item-article-title">{article.title}</h3>
                    <p class="timeline-item-article-body">{article.body}</p>
                </div>
            {/each}
            <div class="timeline-item-salutation">
                <p>Until Next Time, See Ya</p>
            </div>
        </div>
    {/each}
</div>

<style>
    .timeline {
        display: flex;
        flex-direction: column;
        gap: 2rem;
        margin: 1rem;
        margin-top: 0rem;
        border-left: 1px solid rgba(255 255 255 / 25%);
    }

    .timeline > .timeline-item {
        display: flex;
        flex-direction: column;  
        gap: 0.25rem;
    }

    .timeline > .timeline-item > .timeline-item-header {
        position: relative;
    }

    .timeline > .timeline-item > .timeline-item-header > .timeline-item-day {
        position: relative;
    }

    .timeline > .timeline-item > .timeline-item-header > .timeline-item-day > i {
        position: absolute;
        top: 50%;
        left: -0.5px;
        transform: translate(-50%, -50%);
        font-size: 0.5rem;
        color: #94d2bd;
    }

    .timeline > .timeline-item > .timeline-item-header > .timeline-item-day > i:before {
        position: relative;
        z-index: 2; 
    }

    .timeline > .timeline-item > .timeline-item-header > .timeline-item-day > i:after {
        content: "";
        position: absolute;
        left: 50%;
        top: 50%;
        transform: translate(-50%, -50%);
        height: 150%;
        width: 150%;
        background-color: #001219;
        z-index: 1;
    }

    .timeline > .timeline-item > .timeline-item-header > .timeline-item-day > h2 {
        padding-left: 1rem;
        font-size: 2rem;
        font-weight: 900;
        color: #94d2bd;
        line-height: 2.4rem;
    }

    .timeline > .timeline-item > .timeline-item-header > .timeline-item-timestamp {
        padding-left: 1rem;
    }

    .timeline > .timeline-item > .timeline-item-salutation {
        display: flex;
        align-items: center;
        position: relative;
        padding: 0.5rem 1rem;
        padding-left: 1.5rem;
    }

    .timeline > .timeline-item > .timeline-item-salutation:after {
        content: "";
        height: 1px;
        width: 1rem;
        position: absolute;
        left: 0rem;
        top: 50%; 
        border-top: 1px dashed rgba(255 255 255 / 25%);
    }
</style>
