<script lang="ts">
	import { Accordion, AccordionItem } from '@skeletonlabs/skeleton';

	const questionData = [
		'What is your refund policy?',
		'How can I contact customer support?',
		'Do you offer promotions or discounts?',
		'What payment methods do you accept?',
		"I'm a developer - how can I work with SOS?"
	];

	const answerData = [
		'Please contact support at contact.tropicalsos@gmail.com if your game refuses to launch or is not behaving as advertised. We will issue a full refund upon purchase verification.',
		'For inquries, please reach out to us on TikTok, Instagram, X (Twitter), or Email at contact.tropicalsos@gmail.com.',
		'No - that being said, if you want free games, contact us to be a playtester.',
		'We use Paypal (Balance, Card, Bank) and Stripe (Credit and Debit Cards) for payment.',
		'Check out the Linktree for the incubation application.'
	];
</script>

<div class="text-center mb-10 text-3xl font-bold font-mono">Frequently Asked Questions</div>
<div class="flex justify-center font-mono">
	<Accordion spacing="space-y-3" hover="" width="max-w-85" centered>
		{#each questionData as item, index}
			<AccordionItem
				class="bg-surface-50-900-token rounded-container-token p-2 border border-surface-300-600-token w-full max-w-md"
			>
				<svelte:fragment slot="summary"><div class="font-bold">{item}</div></svelte:fragment>
				<svelte:fragment slot="content">{answerData[index]}</svelte:fragment>
			</AccordionItem>
		{/each}
	</Accordion>
</div>
