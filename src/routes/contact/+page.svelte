<script>
    import Hero from '$lib/components/Hero.svelte';
</script>

<svelte:head>
    <title>Contact - Archimedes</title>
    <meta name="description" content="Get in touch with Archimedes at Virginia Tech." />
</svelte:head>

<Hero 
    title="Get in Touch"
    dark={true}
/>

<section class="section">
    <div class="container">
        <div class="contact-content">
            <div class="contact-info">
                <h2>Contact Information</h2>
                <div class="contact-item">
                    <h3>Email</h3>
                    <a href="mailto:archimedesvt@gmail.com">archimedesvt@gmail.com</a>
                </div>
                
                <div class="info-links">
                    <p>Before contacting, see our <a href="/faq">FAQ</a> to check if your question has already been answered.</p>
                    <p>For sponsorship inquiries, please visit our <a href="/sponsor">sponsor page</a>.</p>
                </div>
            </div>
            
            <div class="contact-form">
                <h2>Send us a message</h2>
                <form>
                    <input type="text" placeholder="Your Name" required />
                    <input type="email" placeholder="Your Email" required />
                    <select required>
                        <option value="">Select a topic</option>
                        <option value="general">General Inquiry</option>
                        <option value="apply">Application Question</option>
                        <option value="sponsor">Sponsorship</option>
                        <option value="other">Other</option>
                    </select>
                    <textarea placeholder="Your Message" rows="6" required></textarea>
                    <button type="submit" class="btn">Send Message</button>
                </form>
            </div>
        </div>
    </div>
</section>

<style>
    .contact-content {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 4rem;
        max-width: 1000px;
        margin: 0 auto;
    }
    
    .contact-info h2,
    .contact-form h2 {
        color: var(--primary-color);
        margin-bottom: 2rem;
    }
    
    .contact-item {
        margin-bottom: 2rem;
    }
    
    .contact-item h3 {
        color: var(--secondary-color);
        font-size: 1.1rem;
        margin-bottom: 0.5rem;
    }
    
    .contact-item a {
        color: var(--text-dark);
        text-decoration: none;
        font-size: 1.1rem;
    }
    
    .contact-item a:hover {
        color: var(--primary-color);
    }
    
    .info-links {
        margin-top: 2rem;
        padding: 1.5rem;
        background: var(--gray-light);
        border-radius: 8px;
    }
    
    .info-links p {
        margin-bottom: 0.5rem;
    }
    
    .info-links a {
        color: var(--primary-color);
        text-decoration: none;
        font-weight: 600;
    }
    
    .contact-form form {
        display: flex;
        flex-direction: column;
        gap: 1rem;
    }
    
    .contact-form input,
    .contact-form select,
    .contact-form textarea {
        padding: 12px;
        border: 1px solid #ddd;
        border-radius: 4px;
        font-size: 1rem;
        font-family: inherit;
    }
    
    .contact-form button {
        align-self: flex-start;
    }
    
    @media (max-width: 768px) {
        .contact-content {
            grid-template-columns: 1fr;
            gap: 2rem;
        }
    }
</style>