<script>
    import Hero from '$lib/components/Hero.svelte';
    
    let email = '';
    let submitted = false;
    
    function handleSubmit(e) {
        e.preventDefault();
        // Handle form submission here
        submitted = true;
    }
</script>

<svelte:head>
    <title>Apply - Archimedes</title>
    <meta name="description" content="Apply to join Archimedes at Virginia Tech and start your engineering journey." />
</svelte:head>

<Hero 
    title="Apply to Archimedes"
    subtitle="We're glad you're interested."
    image="https://images.squarespace-cdn.com/content/v1/65da7e107ab81564f3ca3dd0/9a13e988-1f0b-4d96-ba20-9cd41eab89f5/infinitum+pic.png"
/>

<section class="section">
    <div class="container">
        <div class="apply-content">
            <div class="info-box">
                <h2>Applications are now closed for 25-26!</h2>
                <p>Please fill out our interest form for updates and instructions on applying to Archimedes. You will automatically be unsubscribed from our mailing list once the recruiting season has ended.</p>
            </div>
            
            {#if !submitted}
                <form class="interest-form" on:submit={handleSubmit}>
                    <h3>Join Our Interest List</h3>
                    <input 
                        type="email" 
                        bind:value={email}
                        placeholder="Enter your email"
                        required
                    />
                    <button type="submit" class="btn">Submit</button>
                </form>
            {:else}
                <div class="success-message">
                    <h3>Thank you!</h3>
                    <p>We've added you to our interest list. You'll receive updates about the next application period.</p>
                </div>
            {/if}
        </div>
    </div>
</section>

<style>
    .apply-content {
        max-width: 600px;
        margin: 0 auto;
    }
    
    .info-box {
        background: var(--gray-light);
        padding: 2rem;
        border-radius: 8px;
        text-align: center;
        margin-bottom: 3rem;
    }
    
    .info-box h2 {
        color: var(--primary-color);
        margin-bottom: 1rem;
    }
    
    .interest-form {
        background: white;
        padding: 2rem;
        border-radius: 8px;
        box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        text-align: center;
    }
    
    .interest-form h3 {
        color: var(--text-dark);
        margin-bottom: 1.5rem;
    }
    
    .interest-form input {
        width: 100%;
        padding: 12px;
        border: 1px solid #ddd;
        border-radius: 4px;
        margin-bottom: 1rem;
        font-size: 1rem;
    }
    
    .success-message {
        background: #4caf50;
        color: white;
        padding: 2rem;
        border-radius: 8px;
        text-align: center;
    }
    
    .success-message h3 {
        margin-bottom: 1rem;
    }
</style>