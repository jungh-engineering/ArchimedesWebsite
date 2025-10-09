<footer class="footer">
    <div class="container">
        <div class="footer-content">
            <div class="footer-section">
                <h4>Archimedes</h4>
                <p>Empowering STEM freshmen at Virginia Tech through hands-on engineering experiences.</p>
            </div>
            
            <div class="footer-section">
                <h4>Quick Links</h4>
                <ul>
                    <li><a href="/about">About</a></li>
                    <li><a href="/design-teams">Design Teams</a></li>
                    <li><a href="/apply">Apply</a></li>
                    <li><a href="/faq">FAQ</a></li>
                </ul>
            </div>
            
            <div class="footer-section">
                <h4>Contact</h4>
                <p>archimedesvt@gmail.com</p>
                <p>Virginia Tech<br>Blacksburg, VA 24061</p>
            </div>
            
            <div class="footer-section">
                <h4>Follow Us</h4>
                <div class="social-links">
                    <a href="#" aria-label="Instagram">Instagram</a>
                    <a href="#" aria-label="LinkedIn">LinkedIn</a>
                    <a href="#" aria-label="Discord">Discord</a>
                </div>
            </div>
        </div>
        
        <div class="footer-bottom">
            <p>&copy; 2024 Archimedes at Virginia Tech. All rights reserved.</p>
        </div>
    </div>
</footer>

<style>
    .footer {
        background-color: var(--dark-bg);
        color: var(--text-light);
        padding: 3rem 0 1rem;
        margin-top: auto;
    }
    
    .footer-content {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        gap: 2rem;
        margin-bottom: 2rem;
    }
    
    .footer-section h4 {
        color: var(--secondary-color);
        margin-bottom: 1rem;
    }
    
    .footer-section ul {
        list-style: none;
    }
    
    .footer-section a {
        color: var(--text-light);
        text-decoration: none;
        transition: color 0.3s ease;
    }
    
    .footer-section a:hover {
        color: var(--secondary-color);
    }
    
    .social-links {
        display: flex;
        gap: 1rem;
    }
    
    .footer-bottom {
        border-top: 1px solid #333;
        padding-top: 1rem;
        text-align: center;
        color: var(--gray-medium);
    }
</style>