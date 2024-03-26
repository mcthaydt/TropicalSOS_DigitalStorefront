<script>
	import HeroHeaderComponent from '../components/HeroHeaderComponent.svelte';
	import ProductComponent from '../components/ProductComponent.svelte';
	import FAQComponent from '../components/FAQComponent.svelte';
	import SubscribeComponent from '../components/SubscribeComponent.svelte';
</script>

<div class="container h-full mx-auto flex justify-center items-center">
	<div class="my-20">
		<HeroHeaderComponent />
		<div class="grid md:grid-cols-1 gap-4 my-20">
			<ProductComponent />
		</div>
		<FAQComponent />
		<SubscribeComponent />
	</div>
</div>
