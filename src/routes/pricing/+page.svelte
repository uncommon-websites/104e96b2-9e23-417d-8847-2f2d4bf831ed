<script lang="ts">
	// Types
	import type { PageProps } from "./$types";

	// Components
	import Features from "$lib/components/layout/Features.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import CallToAction from "$lib/components/layout/CallToAction.svelte";
	import Pricing from "$lib/components/layout/Pricing.svelte";

	// Props
	const { data }: PageProps = $props();
</script>

<Pricing />

<Testimonials
  testimonials={[
    {
      name: "Larissa Schäfer",
      position: "UX designer",
      company: "Köln IT Studio",
      quote: "I've tried every tool, but this actually made a dent in my workdays. Blocking 90 minutes with Acme gave me more than double the output of a usual afternoon.",
      image: "/generated/image-portrait-of-larissa-schfer-a-german-woma.webp"
    },
    {
      name: "Marc Keller",
      position: "operations lead",
      company: "Basa Logistics GmbH",
      quote: "The return is obvious: two hours of deep work for the cost of a cappuccino. I get tasks done instead of circling for hours.",
      image: "/generated/image-portrait-of-marc-keller-a-white-german-m.webp"
    },
    {
      name: "Silvia Levine",
      position: "content strategist",
      company: "LDN Collective",
      quote: "It’s easy, motivating, and there’s no friction. I open Acme when I really need to get moving—works every time.",
      image: "/generated/image-portrait-of-silvia-levine-a-jewish-briti.webp"
    }
  ]}
/>

<CallToAction
  title="A better way to focus—together"
  subtitle="Struggling to stay on task? You’re not alone."
  description="Acme links you with others for virtual focus sessions that bring structure, accountability, and the environment you need to get things done. Live video with peers. Built-in timers. Designed for ADHDers and chronic procrastinators—open to everyone. Try your first session for free and see why over 60% keep coming back."
  imageSrc="/generated/image-a-happy-adult-sitting-at-a-wooden-desk-i.webp"
  callsToAction={[
    {
      href: '/signup',
      label: 'Start your first session free',
      variant: 'primary'
    },
    {
      href: '/pricing',
      label: 'See all plans',
      variant: 'secondary'
    }
  ]}
/>
