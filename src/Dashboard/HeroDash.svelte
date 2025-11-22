<script>
    // Hero section for Prestige Forms
    // Self-contained, responsive layout with CTA buttons and logo image
    export let title = "Build beautiful forms — fast";
    export let subtitle =
        "Create, customize and publish forms in minutes. No code required.";
</script>

<section class="hero" aria-labelledby="hero-title">
    <div class="hero-inner">
        <div class="hero-copy">
            <h1 id="hero-title">{title}</h1>
            <p class="hero-sub">{subtitle}</p>

            <div class="hero-ctas">
                <a class="btn primary" href="#get-started">Get started</a>
                <a class="btn ghost" href="#learn-more">Learn more</a>
            </div>

            <ul class="hero-features" aria-hidden="false">
                <li>Drag & drop editor</li>
                <li>Custom themes</li>
                <li>Analytics & integrations</li>
            </ul>
        </div>

        <div class="hero-visual" aria-hidden="true">
            <!-- Logo / illustrative image from project root -->
            <img src="../../PRESTIGE.png" alt="Prestige logo" />
        </div>
    </div>
</section>

<style>
    .hero {
        padding: 3rem 1rem;
        background: linear-gradient(180deg, #0f172a 0%, #071033 100%);
        color: var(--color-on-dark, #eef2ff);
    }

    .hero-inner {
        max-width: 1100px;
        margin: 0 auto;
        display: flex;
        gap: 2.5rem;
        align-items: center;
        justify-content: space-between;
        flex-wrap: wrap;
    }

    .hero-copy {
        flex: 1 1 420px;
        min-width: 260px;
    }

    h1 {
        font-size: 2rem;
        line-height: 1.05;
        margin: 0 0 0.75rem 0;
        color: #fff;
    }

    .hero-sub {
        margin: 0 0 1.25rem 0;
        color: rgba(255, 255, 255, 0.85);
    }

    .hero-ctas {
        display: flex;
        gap: 0.75rem;
        margin-bottom: 1rem;
    }

    .btn {
        display: inline-block;
        padding: 0.6rem 1rem;
        border-radius: 8px;
        text-decoration: none;
        font-weight: 600;
        border: 1px solid transparent;
    }

    .btn.primary {
        background: linear-gradient(90deg, #7c3aed, #4f46e5);
        color: white;
    }

    .btn.ghost {
        background: transparent;
        color: #e6eefc;
        border-color: rgba(255, 255, 255, 0.08);
    }

    .hero-features {
        display: flex;
        gap: 1rem;
        list-style: none;
        padding: 0;
        margin: 0.5rem 0 0 0;
        color: rgba(255, 255, 255, 0.8);
        flex-wrap: wrap;
    }

    .hero-features li {
        background: rgba(255, 255, 255, 0.03);
        padding: 0.35rem 0.6rem;
        border-radius: 999px;
        font-size: 0.9rem;
    }

    .hero-visual {
        flex: 0 0 320px;
        display: flex;
        align-items: center;
        justify-content: center;
        min-width: 220px;
    }

    .hero-visual img {
        max-width: 100%;
        height: auto;
        border-radius: 12px;
        box-shadow: 0 8px 30px rgba(2, 6, 23, 0.6);
    }

    @media (max-width: 720px) {
        h1 {
            font-size: 1.6rem;
        }
        .hero-inner {
            gap: 1rem;
        }
        .hero-visual {
            order: -1;
            width: 100%;
            display: flex;
            padding-bottom: 1rem;
        }
        .hero-copy {
            width: 100%;
        }
        .hero-ctas {
            flex-direction: column;
            align-items: stretch;
        }
        .btn {
            width: 100%;
            text-align: center;
        }
    }
</style>
