<script>
	import { Input, Label, NumberInput, P } from 'flowbite-svelte';
	import Stack from '../components/Stack.svelte';
	let value = 5;
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section class="container p-4">
	<Stack>

		<Label class="space-y-2">
			<span>Số lượng</span>
			<Input type="number" bind:value>
				<P slot="right" size="xs" color="gray">bao</P>
			</Input>
		</Label>
	</Stack>
</section>
