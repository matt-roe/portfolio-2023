<script>
	import skills from '$lib/Skills';
</script>

<svelte:head>
	<title>Gianmarco Cavallo — About</title>
</svelte:head>

<div class="container">
	<main>
		<h1>About</h1>
		<p>
			I'm a solutions architect, with a full-stack software developer skillset and a passion for data science and machine learning. I gained JavaScript and Python experience from my IT and Sales roles, with a specialty in quickly developing minimum viable product (MVP) prototypes of my solution designs. This rapid development is critical for early communications of technical proof to stakeholders internal or external (clients). Client calls or internal calls with c-suite level staekholders are a common use-case for my rare combination of interpersonal and technical skills.
		</p>
		<h2>Skills</h2>
		{#each Object.entries(skills) as [section, technologies]}
			<ul>
				<li>
					<h4>
						{section}:
					</h4>
					<div class="list">
						{#each technologies as technology}
							<div>
								{technology}
							</div>
						{/each}
					</div>
				</li>
			</ul>
		{/each}
	</main>
</div>

<style>
	.container {
		max-width: 900px;
		padding: 0;
		display: flex;
		justify-content: center;
	}

	main {
		max-width: 100%;
		min-height: 500px;
		text-align: left;
		margin: 0 auto;
		box-sizing: border-box;
	}

	h1 {
		font-weight: 700;
		margin: 0 0 50px 0;
		font-size: 36px;
		text-align: start;
	}

	h2 {
		margin-top: 50px;
	}

	.list {
		display: flex;
		flex-direction: column;
		gap: 30px;
	}

	@media (min-width: 900px) {
		.list {
			flex-direction: row;
		}
		main > h1 {
			font-size: 48px;
		}
	}
</style>
