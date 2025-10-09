<script>
    export let name = '';
    export let competition = '';
    export let description = '';
    export let members = '';
    export let duration = '';
    export let travel = '';
    export let link = '';
    export let linkText = '';
</script>

<div class="team-card">
    <h3>{name}</h3>
    <h4>{competition}</h4>
    <p class="description">{description}</p>
    
    <div class="details">
        <div class="detail-item">
            <strong>Accepted Members:</strong> {members}
        </div>
        <div class="detail-item">
            <strong>Duration:</strong> {duration}
        </div>
        <div class="detail-item">
            <strong>Travel:</strong> {travel}
        </div>
    </div>
    
    {#if link}
        <a href={link} target="_blank" rel="noopener noreferrer" class="learn-more">
            Learn more at {linkText}
        </a>
    {/if}
</div>

<style>
    .team-card {
        background: white;
        border-radius: 8px;
        padding: 2rem;
        box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        transition: transform 0.3s ease, box-shadow 0.3s ease;
    }
    
    .team-card:hover {
        transform: translateY(-5px);
        box-shadow: 0 8px 15px rgba(0,0,0,0.15);
    }
    
    h3 {
        color: var(--primary-color);
        margin-bottom: 0.5rem;
    }
    
    h4 {
        color: var(--secondary-color);
        margin-bottom: 1rem;
        font-size: 1.1rem;
    }
    
    .description {
        margin-bottom: 1.5rem;
        line-height: 1.6;
    }
    
    .details {
        background: var(--gray-light);
        padding: 1rem;
        border-radius: 4px;
        margin-bottom: 1rem;
    }
    
    .detail-item {
        margin-bottom: 0.5rem;
    }
    
    .detail-item:last-child {
        margin-bottom: 0;
    }
    
    .learn-more {
        color: var(--primary-color);
        text-decoration: none;
        font-weight: 600;
        display: inline-flex;
        align-items: center;
        transition: color 0.3s ease;
    }
    
    .learn-more:hover {
        color: var(--secondary-color);
    }
</style>