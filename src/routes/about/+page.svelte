<script>
    import Hero from '$lib/components/Hero.svelte';
    
    const officers = [
        { role: 'President', name: 'Nidhi Gangadharan' },
        { role: 'VP', name: 'Indu Sanil' },
        { role: 'Secretary', name: 'Sophie Atkisson' },
        { role: 'External Treasurer', name: 'Xander Fry' },
        { role: 'External Treasurer', name: 'Kevin Xu' },
        { role: 'Internal Treasurer', name: 'Helen Brown' },
        { role: 'Recruitment/Publicity', name: 'Bella Guereca' },
        { role: 'External Relations', name: 'Ramsey Wondersek' },
        { role: 'Webmaster', name: 'Jung-Min Hong' }
    ];
</script>

<svelte:head>
    <title>About - Archimedes</title>
    <meta name="description" content="Learn about Archimedes at Virginia Tech and our mission to empower STEM freshmen." />
</svelte:head>

<Hero 
    title="About Archimedes"
    subtitle="Who we are"
    image="https://images.squarespace-cdn.com/content/v1/65da7e107ab81564f3ca3dd0/26fd641b-1349-42ab-bae1-890617ad9f37/VT.png"
/>

<section class="section">
    <div class="container">
        <div class="about-content">
            <div class="about-section">
                <h2>Who we are</h2>
                <p>Archimedes is an umbrella organization that encompasses four design teams, each participating in different national-level collegiate STEM competitions. The teams and their respective competitions are managed and operated by upperclassmen leads and guided by Virginia Tech professors and subject matter experts.</p>
            </div>
            
            <div class="about-section">
                <h2>Our mission</h2>
                <p>Archimedes was founded in 2015 on the principle that STEM freshmen are passionate, goal-driven problem solvers who are more than capable of conquering a design challenge. We strive to give freshmen a more in-depth experience than they might find in an upperclassmen-dominated team. Archimedes provides first-year STEM students with the tools, funding, and mentors to excel in their design competitions.</p>
            </div>
            
            <div class="about-section">
                <h2>Meet the team</h2>
                <div class="officers-grid">
                    {#each officers as officer}
                        <div class="officer-card">
                            <h4>{officer.role}</h4>
                            <p>{officer.name}</p>
                        </div>
                    {/each}
                </div>
            </div>
        </div>
    </div>
</section>

<style>
    .about-content {
        max-width: 900px;
        margin: 0 auto;
    }
    
    .about-section {
        margin-bottom: 4rem;
    }
    
    .about-section h2 {
        color: var(--primary-color);
        margin-bottom: 1.5rem;
        text-align: center;
    }
    
    .about-section p {
        font-size: 1.1rem;
        line-height: 1.8;
        text-align: center;
    }
    
    .officers-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
        gap: 2rem;
        margin-top: 2rem;
    }
    
    .officer-card {
        background: var(--gray-light);
        padding: 1.5rem;
        border-radius: 8px;
        text-align: center;
    }
    
    .officer-card h4 {
        color: var(--secondary-color);
        margin-bottom: 0.5rem;
        font-size: 0.9rem;
        text-transform: uppercase;
        letter-spacing: 1px;
    }
    
    .officer-card p {
        font-weight: 600;
        color: var(--text-dark);
    }
</style>