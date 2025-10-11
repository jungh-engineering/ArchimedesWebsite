<script>
    import Hero from '$lib/components/Hero.svelte';
    
    const faqs = [
        {
            question: "Who can apply to Archimedes?",
            answer: "Archimedes is exclusively for Virginia Tech freshmen. All first-year students, regardless of major or experience level, are welcome to apply."
        },
        {
            question: "Do I need prior engineering experience?",
            answer: "No! We welcome students from all backgrounds and experience levels. Our teams are designed to teach you everything you need to know."
        },
        {
            question: "How much time commitment is required?",
            answer: "Most teams meet 2-3 times per week, with additional workshop time as needed. The total commitment is typically 8-10 hours per week."
        },
        {
            question: "Is there a membership fee?",
            answer: "No, there is no membership fee. All materials, tools, and travel expenses (where applicable) are covered by Archimedes."
        },
        {
            question: "Can I join multiple teams?",
            answer: "Due to the time commitment required for each team, members can only participate in one design team per year."
        },
        {
            question: "When do applications open?",
            answer: "Applications typically open in early September for the following academic year. Join our mailing list to be notified when applications open."
        },
        {
            question: "What happens after I apply?",
            answer: "After submitting your application, you may be invited for an interview. Final decisions are typically made within two weeks of the application deadline."
        },
        {
            question: "Do I get academic credit?",
            answer: "While Archimedes itself doesn't offer academic credit, some teams' work can count towards certain course requirements. Check with your academic advisor."
        }
    ];
    
    let openItems = {};
    
    function toggleItem(index) {
        openItems[index] = !openItems[index];
    }
</script>

<svelte:head>
    <title>FAQ - Archimedes</title>
    <meta name="description" content="Frequently asked questions about Archimedes at Virginia Tech." />
</svelte:head>

<Hero 
    title="Frequently Asked Questions"
    subtitle="Everything you need to know about joining Archimedes"
    dark={true}
/>

<section class="section">
    <div class="container">
        <div class="faq-content">
            {#each faqs as faq, index}
                <div class="faq-item" class:open={openItems[index]}>
                    <button class="faq-question" on:click={() => toggleItem(index)}>
                        <span>{faq.question}</span>
                        <span class="icon">{openItems[index] ? '−' : '+'}</span>
                    </button>
                    {#if openItems[index]}
                        <div class="faq-answer">
                            <p>{faq.answer}</p>
                        </div>
                    {/if}
                </div>
            {/each}
            
            <div class="more-questions">
                <h3>Still have questions?</h3>
                <p>Feel free to reach out to us at <a href="mailto:archimedesvt@gmail.com">archimedesvt@gmail.com</a> or visit our <a href="/contact">contact page</a>.</p>
            </div>
        </div>
    </div>
</section>

<style>
    .faq-content {
        max-width: 800px;
        margin: 0 auto;
    }
    
    .faq-item {
        background: white;
        border-radius: 8px;
        margin-bottom: 1rem;
        box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        overflow: hidden;
        transition: all 0.3s ease;
    }
    
    .faq-item.open {
        box-shadow: 0 4px 8px rgba(0,0,0,0.15);
    }
    
    .faq-question {
        width: 100%;
        padding: 1.5rem;
        background: white;
        border: none;
        text-align: left;
        font-size: 1.1rem;
        font-weight: 600;
        cursor: pointer;
        display: flex;
        justify-content: space-between;
        align-items: center;
        transition: background-color 0.3s ease;
    }
    
    .faq-question:hover {
        background-color: var(--gray-light);
    }
    
    .icon {
        font-size: 1.5rem;
        color: var(--primary-color);
    }
    
    .faq-answer {
        padding: 0 1.5rem 1.5rem;
        animation: slideDown 0.3s ease;
    }
    
    .faq-answer p {
        line-height: 1.6;
        color: var(--text-dark);
    }
    
    .more-questions {
        margin-top: 3rem;
        text-align: center;
        padding: 2rem;
        background: var(--gray-light);
        border-radius: 8px;
    }
    
    .more-questions h3 {
        color: var(--primary-color);
        margin-bottom: 1rem;
    }
    
    .more-questions a {
        color: var(--primary-color);
        text-decoration: none;
        font-weight: 600;
    }
    
    .more-questions a:hover {
        text-decoration: underline;
    }
    
    @keyframes slideDown {
        from {
            opacity: 0;
            transform: translateY(-10px);
        }
        to {
            opacity: 1;
            transform: translateY(0);
        }
    }
</style>