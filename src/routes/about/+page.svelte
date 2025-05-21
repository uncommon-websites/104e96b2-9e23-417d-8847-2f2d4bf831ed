<script lang="ts">
	// Components
	import CallToAction from "$lib/components/layout/CallToAction.svelte";

	// Icons
	import StakeholderGrid from "$lib/components/layout/StakeholderGrid.svelte";
	import Story from "./Story.svelte";
	import SecondaryHero from "$lib/components/layout/hero-sections/SecondaryHero.svelte";
	import Culture from "$lib/components/layout/Culture.svelte";

	// Constants
	const values = [
  {
    title: "Support, not perfection",
    description: "We celebrate real progress—messy, imperfect, and human. Everyone who joins Acme belongs here."
  },
  {
    title: "Mission-driven work",
    description: "We’re here to help people do their best work. Everything we do makes focus and well-being more accessible."
  },
  {
    title: "Empathy at the core",
    description: "No judgment, just understanding. We value each person’s unique brain and way of working."
  },
  {
    title: "Collaboration over competition",
    description: "We show up for each other. When one succeeds, we all do."
  },
  {
    title: "Keep it simple",
    description: "We remove friction and overcomplication. Focus thrives in clear, supportive spaces."
  }
];
</script>

<SecondaryHero
	title="Focus better, together"
	subtitle="Virtual co-working sessions that help you stay on task and feel supported"
	imageSrc="/mockups/airport-screen-1747842133225.png"
/>

<!-- Story Section -->
<Story
	paragraphs={[
		"It started with distraction. Jane, a psychologist and life coach, struggled to find tools that truly helped her ADHD clients—and herself—stay focused. Thomas and Lucy faced the same challenges in their high-pressure jobs. Tired of unreliable hacks and quick fixes, the three friends decided to create a solution that actually worked. One rooted in structure, empathy, and community. So they built Acme.",
		"Acme is a virtual space where people struggling with focus can finally get things done—together. In real-time focus sessions, users work alongside others with similar challenges. No pressure, just quiet accountability. Whether you have ADHD, procrastinate often, or simply feel overwhelmed, it’s a calm, supportive environment to stay on track.",
		"We believe focus shouldn't depend on willpower alone. Everyone hits mental walls. Acme is here to make getting past them a little easier. We're starting in Germany but building for a global community—because no one should have to battle focus problems alone."
	]}
/>

<!-- Our Culture Section -->
<Culture {values} />

<!-- StakeholderGrid Section -->
<StakeholderGrid
  stakeholderType="team"
  title="Our founders"
  subtitle="Meet the people behind Acme Inc"
  stakeholders={[
    {
      name: "Jane Doe",
      position: "CEO, Psychologist & Life Coach",
      bio: "Jane leads Acme with deep empathy for the daily realities of ADHD and focus struggles. She ensures everything we build is grounded in science and kindness.",
      image: "/generated/image-a-headshot-of-a-female-psychologist-and-.webp"
    },
    {
      name: "Thomas Müller",
      position: "CSO, Ex-McKinsey",
      bio: "Thomas brings rigorous strategy and a drive to solve complex problems, helping Acme grow thoughtfully and with purpose.",
      image: "/generated/image-a-headshot-of-a-german-male-business-exe.webp"
    },
    {
      name: "Lucy Rocks",
      position: "CTO, Fullstack Developer",
      bio: "Lucy makes sure every session runs seamlessly so users can focus, not fight with tech. She’s obsessed with building tools that truly help."
      ,image: "/generated/image-a-headshot-of-a-woman-software-engineer-.webp"
    }
  ]}
/>

<!-- No investors to display -->

<!-- CTA Section -->
<CallToAction
	title="Ready to collaborate?"
	subtitle="Let's create something amazing"
	description="Join the companies already leveraging our expertise to transform their digital presence and achieve their business goals."
/>
