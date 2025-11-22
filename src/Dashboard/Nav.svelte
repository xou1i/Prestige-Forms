<nav class="navbar">
    <div class="nav-container">
        <a href="/" class="nav-logo">Logo</a>
        <ul class="nav-menu">
            <li class="nav-item">
                <a href="/" class="nav-link">Home</a>
            </li>
            <li class="nav-item">
                <a href="/about" class="nav-link">About</a>
            </li>
            <li class="nav-item">
                <a href="/services" class="nav-link">Services</a>
            </li>
            <li class="nav-item">
                <a href="/contact" class="nav-link">Contact</a>
            </li>
        </ul>
    </div>
</nav>

<style>
    .navbar {
        background-color: #333;
        padding: 0.5rem 0;
    }

    .nav-container {
        max-width: 1200px;
        margin: 0 auto;
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 0 2rem;
    }

    .nav-logo {
        color: white;
        font-size: 1.5rem;
        font-weight: bold;
        text-decoration: none;
    }

    .nav-menu {
        display: flex;
        list-style: none;
        margin: 0;
        padding: 0;
        gap: 2rem;
    }

    .nav-link {
        color: white;
        text-decoration: none;
        transition: color 0.3s;
    }

    .nav-link:hover {
        color: #ddd;
    }
</style>