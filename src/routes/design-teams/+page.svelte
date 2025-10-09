<script>
    import Hero from '$lib/components/Hero.svelte';
    import TeamCard from '$lib/components/TeamCard.svelte';
    
    const teams = [
        {
            name: 'Juvo',
            competition: 'RESNA Student Design Competition',
            description: 'Founded in 2018, Juvo uses engineering to help the community. Freshmen are tasked with designing a solution for someone in the disabled community. In the past, Juvo has created solutions for accessibility in production, wheelchair disabilities, motor impairments, and more!',
            members: '8',
            duration: '9 months',
            travel: 'No travel',
            link: 'https://www.resna.org/Events/2024-Student-Design-Challenge',
            linkText: 'resna.org'
        },
        {
            name: 'Astra',
            competition: 'NASA Micro-g NExT',
            description: 'Founded in 2015, Astra challenges students to design, build, and test a device related to space exploration. Astra has built devices such as a spacesuit cooling system, a lunar anchoring device, an autonomous rescue boat, and more!',
            members: '7',
            duration: '10 months',
            travel: 'Covered travel',
            link: 'https://www.nasa.gov/learning-resources/micro-g-neutral-buoyancy-experiment-designteams/',
            linkText: 'nasa.gov'
        },
        {
            name: 'Infinitum',
            competition: 'Microsoft Imagine Cup',
            description: 'Founded in 2020, Infinitum offers an exciting opportunity to develop and build hardware and software addressing real-world problems. Infinitum has tackled problems such as food recognition in fridges, restaurant food waste management, and more!',
            members: '7-8',
            duration: '9 months',
            travel: 'No travel',
            link: 'https://imaginecup.microsoft.com/en-us',
            linkText: 'microsoft.com'
        },
        {
            name: 'Terra',
            competition: 'ASME Student Design Competition',
            description: 'Founded in 2024, Terra provides students with the opportunity to design, build, drive, and compete a robot based on the season\'s game manual and rules. Terra is Arch