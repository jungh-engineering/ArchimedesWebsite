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
    background: var(--white);
    border-radius: var(--radius-md);
    padding: 2rem;
    box-shadow: 0 8px 20px rgba(0, 0, 0, 0.08);
    border: 1px solid rgba(0, 0, 0, 0.05);
    transition: transform var(--tr), box-shadow var(--tr), border-color var(--tr);
  }

  .team-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 14px 30px rgba(0, 0, 0, 0.12);
    border-color: rgba(255, 200, 0, 0.3);
  }

  h3 {
    color: var(--archimedes-yellow-bright);
    font-weight: 800;
    margin-bottom: 0.5rem;
  }

  h4 {
    color: var(--steel);
    margin-bottom: 1rem;
    font-size: 1.1rem;
    opacity: 0.9;
  }

  .description {
    margin-bottom: 1.5rem;
    line-height: 1.6;
    color: var(--steel);
  }

  .details {
    background: var(--halogen-haze);
    padding: 1rem;
    border-radius: var(--radius-sm);
    margin-bottom: 1.25rem;
    border: 1px solid rgba(0, 0, 0, 0.05);
  }

  .detail-item {
    margin-bottom: 0.5rem;
    color: var(--steel);
    font-size: 0.95rem;
  }

  .detail-item strong {
    color: var(--archimedes-yellow-bright);
    font-weight: 700;
  }

  .detail-item:last-child {
    margin-bottom: 0;
  }

  .learn-more {
    color: var(--archimedes-yellow);
    text-decoration: none;
    font-weight: 700;
    letter-spacing: 0.02em;
    display: inline-flex;
    align-items: center;
    transition: color var(--tr);
  }

  .learn-more:hover {
    color: var(--archimedes-yellow-bright);
  }

  @media (max-width: 768px) {
    .team-card {
      padding: 1.5rem;
    }
  }
</style>
