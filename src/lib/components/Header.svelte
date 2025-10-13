<script>
    import { page } from '$app/stores';
    
    let mobileMenuOpen = false;
    
    function toggleMobileMenu() {
        mobileMenuOpen = !mobileMenuOpen;
    }
</script>

<header class="header">
    <nav class="navbar">
        <div class="container nav-container">
            <a href="/" class="logo">
                <span class="logo-text">ARCHIMEDES</span>
                <span class="logo-subtitle">at Virginia Tech</span>
            </a>
            
            <button class="mobile-menu-toggle" on:click={toggleMobileMenu}>
                <span></span>
                <span></span>
                <span></span>
            </button>
            
            <ul class="nav-menu" class:active={mobileMenuOpen}>
                <li><a href="/" class:active={$page.url.pathname === '/'}>Home</a></li>
                <li><a href="/about" class:active={$page.url.pathname === '/about'}>About</a></li>
                <li><a href="/design-teams" class:active={$page.url.pathname === '/design-teams'}>Design Teams</a></li>
                <li><a href="/apply" class:active={$page.url.pathname === '/apply'}>Apply</a></li>
                <li><a href="/faq" class:active={$page.url.pathname === '/faq'}>FAQ</a></li>
                <li><a href="/sponsor" class:active={$page.url.pathname === '/sponsor'}>Sponsor</a></li>
                <li><a href="/contact" class:active={$page.url.pathname === '/contact'}>Contact</a></li>
            </ul>
        </div>
    </nav>
</header>

<style>
    .header {
        background: #fff;
        box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        position: sticky;
        top: 0;
        z-index: 1000;
    }
    
    .navbar {
        padding: 1rem 0;
    }
    
    .nav-container {
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
    
    .logo {
        display: flex;
        flex-direction: column;
        text-decoration: none;
        color: var(--primary-color);
    }
    
    .logo-text {
        font-size: 1.5rem;
        font-weight: 900;
        letter-spacing: 2px;
    }
    
    .logo-subtitle {
        font-size: 0.8rem;
        font-weight: 400;
        color: var(--gray-medium);
    }
    
    .nav-menu {
        display: flex;
        list-style: none;
        gap: 2rem;
        align-items: center;
    }
    
    .nav-menu a {
        color: var(--text-dark);
        text-decoration: none;
        font-weight: 500;
        transition: color 0.3s ease;
        padding: 0.5rem 0;
    }
    
    .nav-menu a:hover,
    .nav-menu a.active {
        color: var(--primary-color);
    }
    
    .mobile-menu-toggle {
        display: none;
        flex-direction: column;
        background: transparent;
        border: none;
        cursor: pointer;
        padding: 0;
    }
    
    .mobile-menu-toggle span {
        width: 25px;
        height: 3px;
        background: var(--text-dark);
        margin: 3px 0;
        transition: 0.3s;
    }
    
    @media (max-width: 768px) {
        .mobile-menu-toggle {
            display: flex;
        }
        
        .nav-menu {
            position: fixed;
            left: -100%;
            top: 70px;
            flex-direction: column;
            background-color: white;
            width: 100%;
            padding: 2rem 0;
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
            transition: 0.3s;
        }
        
        .nav-menu.active {
            left: 0;
        }
    }
</style>