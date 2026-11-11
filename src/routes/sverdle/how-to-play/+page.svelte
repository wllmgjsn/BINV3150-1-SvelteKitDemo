<svelte:head>
	<title>Comment jouer à Sverdle</title>
	<meta name="description" content="Comment jouer à Sverdle" />
</svelte:head>

<div class="text-column">
	<h1>Comment jouer à Sverdle</h1>

	<p>
		Sverdle est un clone de <a href="https://www.nytimes.com/games/wordle/index.html">Wordle</a>, le
		jeu de devinettes de mots. Pour jouer, saisissez un mot anglais de cinq lettres. Par exemple :
	</p>

	<div class="example">
		<span class="close">r</span>
		<span class="missing">i</span>
		<span class="close">t</span>
		<span class="missing">z</span>
		<span class="exact">y</span>
	</div>

	<p>
		Le <span class="exact">y</span> est à la bonne place. Le <span class="close">r</span> et le
		<span class="close">t</span>
		sont les bonnes lettres, mais mal placées. Les autres lettres sont incorrectes et peuvent être écartées.
		Tentons une autre proposition :
	</p>

	<div class="example">
		<span class="exact">p</span>
		<span class="exact">a</span>
		<span class="exact">r</span>
		<span class="exact">t</span>
		<span class="exact">y</span>
	</div>

	<p>Cette fois, c'est la bonne réponse ! Vous avez <strong>six</strong> essais pour trouver le mot.</p>

	<p>
		Contrairement au Wordle original, Sverdle s'exécute sur le serveur plutôt que dans le navigateur, ce qui
		rend la triche impossible. Il utilise <code>&lt;form&gt;</code> et des cookies pour envoyer les données, ce
		qui signifie que vous pouvez même jouer avec JavaScript désactivé !
	</p>
</div>

<style>
	span {
		display: inline-flex;
		justify-content: center;
		align-items: center;
		font-size: 0.8em;
		width: 2.4em;
		height: 2.4em;
		background-color: white;
		box-sizing: border-box;
		border-radius: 2px;
		border-width: 2px;
		color: rgba(0, 0, 0, 0.7);
	}

	.missing {
		background: rgba(255, 255, 255, 0.5);
		color: rgba(0, 0, 0, 0.5);
	}

	.close {
		border-style: solid;
		border-color: var(--color-theme-2);
	}

	.exact {
		background: var(--color-theme-2);
		color: white;
	}

	.example {
		display: flex;
		justify-content: flex-start;
		margin: 1rem 0;
		gap: 0.2rem;
	}

	.example span {
		font-size: 1.4rem;
	}

	p span {
		position: relative;
		border-width: 1px;
		border-radius: 1px;
		font-size: 0.4em;
		transform: scale(2) translate(0, -10%);
		margin: 0 1em;
	}
</style>
