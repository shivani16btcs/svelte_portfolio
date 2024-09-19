<script lang="ts">
	export let link: string | null;
	export let text: string;
</script>

{#if link}
	<a href={link} class="realistic-button">
		{text}
	</a>
{:else}
	<button class="realistic-button">
		{text}
	</button>
{/if}

<style>
	.realistic-button {
		background: linear-gradient(145deg, #204a7d, #1e3551);
		color: white;
		padding: 12px 24px;
		border-radius: 12px;
		box-shadow: 6px 6px 12px rgba(0, 0, 0, 0.2), -4px -4px 8px rgba(255, 255, 255, 0.1);
		font-weight: 600;
		text-transform: uppercase;
		letter-spacing: 1px;
		transition: all 0.3s ease-in-out;
		display: inline-block;
		margin-top: 1.5rem;
	}

	.realistic-button:hover {
		background: linear-gradient(145deg, #1e3551, #204a7d);
		box-shadow: 8px 8px 16px rgba(0, 0, 0, 0.3), -6px -6px 12px rgba(255, 255, 255, 0.2);
		transform: translateY(-4px);
	}
</style>
