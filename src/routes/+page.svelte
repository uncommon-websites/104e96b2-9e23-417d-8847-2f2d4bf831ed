<script lang="ts">
	// Components
	import UseCases from "$lib/components/layout/UseCases.svelte";
	import Summary from "$lib/components/layout/Summary.svelte";
	import Features from "$lib/components/layout/Features.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import CallToAction from "$lib/components/layout/CallToAction.svelte";
	import AboutTeaser from "$lib/components/layout/AboutTeaser.svelte";
	import LogoScroller from "$lib/components/layout/LogoScroller.svelte";
	import Hero from "$lib/components/layout/hero-sections/Hero.svelte";
</script>

<Hero
	title="Elevate your business with thoughtful design"
	subtitle="Solutions that enhance user experience, and improve visual communication."
	imageSrc="/sample.png"
	generating
/>
<LogoScroller label="" generating />

<Summary
	generating
	title="What we do"
	text="Our technology delivers measurable results through secure, adaptable solutions that directly increase productivity and drive growth."
/>

<Testimonials
	generating
	testimonials={[
		{
			name: "Jane Smith",
			position: "CTO",
			company: "Tech Innovations",
			quote:
				"Their cutting-edge automation boosted our productivity by 35%.\nThe intuitive interface reduced training time and improved team adoption.",
			image:
				"https://images.unsplash.com/photo-1571513722275-4b41940f54b8?q=80&w=3687&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
		},
		{
			name: "John Doe",
			position: "Director of Operations",
			company: "Global Solutions",
			quote:
				"Their robust security protocols gave us confidence in handling sensitive data.\nThe 24/7 support team resolved issues within hours, not days.",
			image:
				"https://images.unsplash.com/photo-1600603405959-6d623e92445c?q=80&w=3687&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
		},
		{
			name: "Sarah Johnson",
			position: "Product Manager",
			company: "Future Systems",
			quote:
				"The scalable platform grew seamlessly with our business needs.\nTheir customization options allowed us to tailor solutions perfectly to our workflows.",
			image:
				"https://images.unsplash.com/photo-1531123897727-8f129e1688ce?q=80&w=3687&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
		}
	]}
/>

<Features
	generating
	title="Features"
	subtitle="Some features"
	features={[
		{
			title: "Streamlined Workflows",
			description:
				"Automate repetitive tasks and connect systems to improve productivity with our industry-leading 87% time savings."
		},
		{
			title: "Data Analysis",
			description:
				"Extract meaningful insights from your data with powerful analytical tools backed by proprietary AI algorithms that are 3x more accurate than competitors."
		},
		{
			title: "Secure Collaboration",
			description:
				"Work together seamlessly while maintaining strict data privacy standards with our zero-knowledge architecture and military-grade encryption."
		}
	]}
/>

<UseCases
    title="Use cases"
    subtitle="Ways people use Acme to get things done"
    useCases={[
        {
            title: "Overcoming procrastination",
            description: "Can't get started no matter how urgent the task? Join a session with others tackling their own to-dos—it lowers the pressure and helps you break through the mental block.",
            image: "/generated/image-a-young-adult-with-adhd-beginning-their-.webp",
            link: {
                href: "/use-cases/overcoming-procrastination",
                label: "Learn more"
            }
        },
        {
            title: "Staying accountable with real human faces",
            description: "It's easy to put things off when no one's watching. Acme gives you structure and accountability through live peer sessions so you follow through more often.",
            image: "/generated/image-a-small-group-of-adults-gathered-in-a-co.webp",
            link: {
                href: "/use-cases/accountability-partners",
                label: "Learn more"
            }
        },
        {
            title: "Getting focused during crunch time",
            description: "Deadlines piling up? Book focused, time-boxed sprints with peers to stay on task and make real progress when it matters most.",
            image: "/generated/image-an-individual-working-intently-racing-ag.webp",
            link: {
                href: "/use-cases/focus-sprints",
                label: "Learn more"
            }
        }
    ]}
/>

<AboutTeaser />
<CallToAction
  title="Better focus, together"
  subtitle="Get the support you need, every session"
  description="Join virtual focus sessions with peers who get it. Our supportive community helps you start, stay on track, and finish—especially if you have ADHD or struggle with procrastination."
  imageSrc="/generated/image-a-cheerful-young-adult-german-woman-work.webp"
  callsToAction={[
    {
      href: '/sign-up',
      label: 'Try your first session free',
      variant: 'primary'
    },
    {
      href: '/how-it-works',
      label: 'How it works',
      variant: 'secondary'
    }
  ]}
/>
