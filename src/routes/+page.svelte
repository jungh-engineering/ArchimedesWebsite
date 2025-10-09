<script>
    import Hero from '$lib/components/Hero.svelte';
</script>

<svelte:head>
    <title>Archimedes at Virginia Tech</title>
    <meta name="description" content="We are a student organization that hosts four design teams exclusively for STEM freshmen at Virginia Tech." />
</svelte:head>

<Hero 
    title="Jump-start your STEM career early."
    subtitle="Get the best hands-on engineering experience right from the start, here at Virginia Tech. Open to freshmen only."
    image="https://images.squarespace-cdn.com/content/v1/65da7e107ab81564f3ca3dd0/10dee911-c63a-4369-8492-cabad175072e/52974284471_273d239257_k.jpg"
>
    <a href="/apply" class="btn">Apply Now</a>
</Hero>

<section class="section">
    <div class="container">
        <div class="content-grid">
            <div class="content-block">
                <h2>Who are we?</h2>
                <p>We are a student organization that hosts four design teams exclusively for Virginia Tech freshmen. Guided by upperclassmen leads and subject-matter experts, freshmen have the unique opportunity to participate in STEM design challenges that feature hands-on work alongside NASA, Microsoft, ASME, and RESNA.</p>
            </div>
            
            <div class="content-block">
                <h2>No experience required.</h2>
                <p>No matter your intended major or experience level, Archimedes is here to accelerate and test your capabilities as an engineer or scientist.</p>
            </div>
            
            <div class="content-block">
                <h2>Why join?</h2>
                <p>Archimedes gives freshmen full creative freedom from the drawing board to the workshop. Members are provided with mentorship, funding, professional development opportunities, and more!</p>
            </div>
        </div>
        
        <div class="image-section">
            <img src="https://images.squarespace-cdn.com/content/v1/65da7e107ab81564f3ca3dd0/64078f72-0a07-4c9e-ab6a-3baa84a40adf/52143452927_5fe171d25e_o.jpg" 
                 alt="Archimedes team working" 
                 class="hero-image" />
        </div>
    </div>
</section>

<style>
    .content-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
        gap: 3rem;
        margin-bottom: 4rem;
    }
    
    .content-block {
        text-align: center;
    }
    
    .content-block h2 {
        color: var(--primary-color);
        margin-bottom: 1rem;
    }
    
    .content-block p {
        font-size: 1.1rem;
        line-height: 1.8;
    }
    
    .image-section {
        margin-top: 4rem;
    }
</style>