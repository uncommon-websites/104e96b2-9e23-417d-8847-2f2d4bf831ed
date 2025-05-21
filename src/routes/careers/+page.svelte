<script lang="ts">
	// Types

	// Components
	import SectionHeader from "$lib/components/layout/SectionHeader.svelte";
	import Culture from "$lib/components/layout/Culture.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import SecondaryHero from "$lib/components/layout/hero-sections/SecondaryHero.svelte";
	import Card from "$lib/components/ui/Card.svelte";
	import JobList, { type JobOpening } from "./JobList.svelte";

	// Icons
	import IconBriefcase from "~icons/lucide/briefcase";
	import IconUsers from "~icons/lucide/users";
	import IconHeart from "~icons/lucide/heart";
	import IconGlobe from "~icons/lucide/globe";

	// Constants
	const SECTION_BASE_CLASSES = "section-py section-px container mx-auto";
	const GRADIENT_BG_CLASSES =
		"bg-gradient-to-br from-gray-50 to-gray-100 dark:from-gray-900 dark:to-gray-800";
	const ICON_CONTAINER_CLASSES =
		"bg-primary-50 text-primary-600 dark:bg-primary-950 dark:text-primary-400 flex items-center justify-center rounded-full";

	const benefits = [
		{
			title: "Flexible Work",
			description: "Remote-first with flexible hours that respect work-life balance.",
			icon: IconBriefcase
		},
		{
			title: "Growth Opportunities",
			description: "Continuous learning with mentorship and education stipends.",
			icon: IconUsers
		},
		{
			title: "Comprehensive Benefits",
			description: "Health coverage, retirement plans, and generous paid time off.",
			icon: IconHeart
		}
	];

	const openings: JobOpening[] = [
		// Engineering
		{
			title: "Senior Frontend Developer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Backend Engineer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Design Engineer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Design
		{
			title: "UX/UI Designer",
			department: "Design",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Product Designer",
			department: "Design",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Product
		{
			title: "Product Manager",
			department: "Product",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Product Analyst",
			department: "Product",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Marketing
		{
			title: "Marketing Specialist",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Content Strategist",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Social Media Manager",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		}
	];

	const employeeTestimonials = [
  {
    name: "Michael Chen",
    position: "Senior Software Engineer",
    company: "Engineering",
    quote:
      "The culture here is open, respectful, and genuinely collaborative. I always feel heard and supported, which makes tackling complex problems so much more rewarding.",
    image: "/generated/image-portrait-of-an-asian-male-software-engin.webp"
  },
  {
    name: "Aisha Thomas",
    position: "Marketing Specialist",
    company: "Marketing",
    quote:
      "Acme Inc encourages real growth. My ideas matter and my manager actively champions my development—it's a place where you can truly own your successes.",
    image: "/generated/image-portrait-of-a-black-female-marketing-spe.webp"
  },
  {
    name: "Taylor Reed",
    position: "Product Manager",
    company: "Product",
    quote:
      "What stands out is the trust and flexibility here. I work with kind, driven people who support each other, and I have flexibility to shape how I work best.",
    image: "/generated/image-portrait-of-a-white-non-binary-product-m.webp"
  }
];

	const processSteps = [
	{
		step: 1,
		title: "Quick intro",
		description: "Send us a few lines about yourself and a link to your work or something you’re proud of."
	},
	{
		step: 2,
		title: "Meet the team",
		description: "If it’s a fit, we’ll set up a friendly 30-min video call to get to know each other."
	},
	{
		step: 3,
		title: "Final chat",
		description: "Have a relaxed conversation with one or two of our co-founders—no gotcha questions."
	}
];

	const values = [
		{
			icon: IconHeart,
			title: "Passion",
			description: "We're driven by a shared passion for innovation and excellence."
		},
		{
			icon: IconUsers,
			title: "Collaboration",
			description: "We believe in teamwork and collaboration to achieve great things."
		},
		{
			icon: IconGlobe,
			title: "Global Impact",
			description: "We're committed to making a positive impact on the world."
		}
	];
</script>

<!-- Hero Section -->

<SecondaryHero
  title="Build better focus, together"
  subtitle="Join a supportive, inclusive team that helps people thrive"
  imageSrc="/generated/image-a-warm-and-inviting-office-setting-with-.webp"
/>

<!-- Why Join Us Section -->
<section class={SECTION_BASE_CLASSES}>
	<SectionHeader title="Focus is hard. We make it easier." subtitle="Work where focus, growth, and support are at the heart of everything we do." />

<p class="mt-6 text-body text-emphasis-low max-w-2xl">Acme Inc helps people stay on task and feel supported through peer-led virtual focus sessions, built with neurodivergent brains in mind—effective for anyone who struggles to concentrate.</p>

<ul class="mt-8 mb-2 text-sm">
  <li class="mb-1">• 60% of ADHD users return for more sessions</li>
  <li class="mb-1">• User satisfaction: 4.4/5</li>
  <li class="mb-1">• Net Promoter Score (NPS): 9.38</li>
  <li>• 145 sessions booked—before launching marketing</li>
</ul>

<SectionHeader class="mt-16" title="Why join us" subtitle="Shape a product that truly helps people and grow as we grow." />
<div class="mt-8 grid gap-4 md:grid-cols-3">
	{#each benefits as benefit}
		<Card {...benefit} />
	{/each}
</div>
</section>

<!-- Culture Section -->
<Culture {values} />
<p class="mt-6 text-body text-emphasis-low max-w-2xl">We are building a place where neurodiversity isn’t just accepted—it’s a strength. We value open communication, honest feedback, and a bias toward action. This is a team that celebrates quirky ideas, runs fast experiments, and doesn’t waste time on pointless meetings. We care about each other as much as the impact we make for our users.</p>

<Testimonials testimonials={employeeTestimonials} />

<!-- Application Process -->
<section class={SECTION_BASE_CLASSES}>
	<div class="mx-auto">
		<h2 class="text-title1 mb-16">Our application process</h2>
<p class="mb-8 text-body text-emphasis-low max-w-2xl">We like to keep things fast, friendly, and low-stress. You’ll always hear back from us within five business days after your first message.</p>

		<div class="grid gap-12 md:grid-cols-3">
			{#each processSteps as { step, title, description }, i}
				<div class="flex flex-col">
					<div class="{ICON_CONTAINER_CLASSES} mb-6 size-11">
						<span class="text-headline">{step}</span>
					</div>
					<h3 class="text-headline mb-3">{title}</h3>
					<p class="text-body text-emphasis-low">{description}</p>
				</div>
			{/each}
		</div>
	</div>
</section>
<!-- Current Openings Section -->
<section class={GRADIENT_BG_CLASSES}>
	<div class="section-px section-py container mx-auto grid w-full items-start lg:grid-cols-2">
		<SectionHeader title="Current openings" subtitle="Find your perfect role" />

		<JobList {openings} />
	</div>
</section>
