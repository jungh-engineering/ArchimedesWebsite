<script>
  import { page } from '$app/stores';
  let mobileMenuOpen = false;
  const toggleMobileMenu = () => (mobileMenuOpen = !mobileMenuOpen);
</script>

<header class="nav">
  <nav class="container nav__inner">
    <!-- Brand -->
    <a href="/" class="brand">
              <div class="image-section">
            <img src="/logoheader.png" 
                 alt="logoheader" 
                 class="hero-image" />
        </div>
    </a>

    <!-- Mobile toggle -->
    <button class="hamburger" on:click={toggleMobileMenu} aria-label="Toggle navigation" aria-expanded={mobileMenuOpen}>
      <span class:open={mobileMenuOpen}></span>
      <span class:open={mobileMenuOpen}></span>
      <span class:open={mobileMenuOpen}></span>
    </button>

    <!-- Desktop / Mobile menu -->
    <ul class="menu" class:open={mobileMenuOpen}>
      <li><a href="/" class:current={$page.url.pathname === '/'}>Home</a></li>
      <li><a href="/about" class:current={$page.url.pathname === '/about'}>About</a></li>
      <li><a href="/design-teams" class:current={$page.url.pathname === '/design-teams'}>Design Teams</a></li>
      <li><a href="/apply" class:current={$page.url.pathname === '/apply'}>Apply</a></li>
      <li><a href="/faq" class:current={$page.url.pathname === '/faq'}>FAQ</a></li>
      <li><a href="/sponsor" class:current={$page.url.pathname === '/sponsor'}>Sponsor</a></li>
      <li><a href="/contact" class:current={$page.url.pathname === '/contact'}>Contact</a></li>
    </ul>
  </nav>
</header>

<style>
  .image-section {
    height: 68px;
    display: flex;
    align-items: center;
  }

  .image-section img {
    height: 52px;
    width: auto;
    object-fit: contain;
    border-radius: var(--radius-md);
  }

  /* Uses globals: .nav base styles, colors, container spacing, link underline hover */
  .nav {
    /* globals already provide sticky dark bar; this ensures good contrast */
    background: rgba(25, 43, 46, 0.9);
    backdrop-filter: blur(6px);
    border-bottom: 1px solid rgba(255, 255, 255, 0.06);
  }

  .nav__inner {
    height: 68px;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  /* Brand lockup */
  .brand {
    display: flex;
    align-items: center;
    text-decoration: none;
    color: var(--text-on-dark);
  }
  .brand__title {
    font-weight: 900;
    letter-spacing: 0.18em;
    font-size: 1.05rem;
  }
  .brand__sub {
    font-family: var(--font-secondary);
    font-size: 0.78rem;
    color: rgba(255, 255, 255, 0.75);
  }

  /* Menu */
  .menu {
    list-style: none;
    display: flex;
    gap: 1.75rem;
    align-items: center;
  }

  .menu a {
    color: var(--text-on-dark);
    text-decoration: none;
    font-weight: 600;
    padding: 10px 0;
    transition: color var(--tr), opacity var(--tr);
    /* underline on hover comes from globals: .nav a::after */
  }
  .menu a:hover { color: var(--luminal-yellow); }
  .menu a.current {
    color: var(--archimedes-yellow);
  }
  .menu a.current::after {
    transform: scaleX(1); /* show the yellow underline from globals */
  }

  /* Hamburger (mobile) */
  .hamburger {
    display: none;
    flex-direction: column;
    justify-content: center;
    gap: 5px;
    width: 36px;
    height: 36px;
    background: transparent;
    border: 1px solid rgba(255, 255, 255, 0.12);
    border-radius: var(--radius-sm);
    cursor: pointer;
    padding: 6px;
    transition: border-color var(--tr), background var(--tr);
  }
  .hamburger:hover {
    border-color: var(--archimedes-yellow);
    background: rgba(255, 200, 0, 0.06);
  }
  .hamburger span {
    display: block;
    width: 100%;
    height: 2px;
    background: var(--archimedes-yellow);
    transition: transform var(--tr), opacity var(--tr);
  }
  /* Simple X animation */
  .hamburger span.open:nth-child(1) { transform: translateY(7px) rotate(45deg); }
  .hamburger span.open:nth-child(2) { opacity: 0; }
  .hamburger span.open:nth-child(3) { transform: translateY(-7px) rotate(-45deg); }

  /* Mobile behavior */
  @media (max-width: 900px) {
    .hamburger { display: flex; }

    .image-section {
      display: none; /* Hide logo on mobile to save space */
    }

    .menu {
      position: fixed;
      inset: 68px 0 0 0;
      background: var(--steel);
      border-top: 1px solid rgba(255, 255, 255, 0.06);
      box-shadow: var(--shadow-lg);
      flex-direction: column;
      align-items: flex-start;
      padding: 20px 24px 28px;
      gap: 0.25rem;
      transform: translateX(-100%);
      transition: transform var(--tr);
      z-index: 40;
    }
    .menu.open { transform: translateX(0); }

    .menu li { width: 100%; }
    .menu a {
      width: 100%;
      padding: 12px 4px;
      border-bottom: 1px solid rgba(255, 255, 255, 0.06);
    }
  }
</style>
