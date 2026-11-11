<script lang="ts">
	import { resolve } from '$app/paths';
</script>

<svelte:head>
	<title>À propos</title>
	<meta name="description" content="À propos de cette application" />
</svelte:head>

<div class="text-column">
	<h1>À propos de cette application</h1>

	<p>
		Ceci est une application <a href="https://svelte.dev/docs/kit">SvelteKit</a>. Vous pouvez créer la vôtre
		en saisissant la commande suivante dans votre terminal et en suivant les instructions :
	</p>

	<pre>npx sv create</pre>

	<p>
		La page que vous consultez est du pur HTML statique, sans aucune interactivité côté client.
		Pour cette raison, nous n'avons pas besoin de charger de JavaScript. Essayez d'afficher le code source de la page,
		ou d'ouvrir l'onglet réseau des outils de développement et de recharger la page.
	</p>

	<p>
		La page <a href={resolve('/sverdle')}>Sverdle</a> illustre le chargement de données et la gestion des formulaires dans SvelteKit.
		Essayez-la avec JavaScript désactivé !
	</p>
</div>
